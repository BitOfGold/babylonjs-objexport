##Export and Download Meshes from BABYLON.js in .OBJ + .MTL format.##

**Now part of BABYLON.js, this repo is abadoned.**

Here is the exporter:
https://github.com/BabylonJS/Babylon.js/blob/master/dist/serializers/babylon.objSerializer.js

The source is here:
https://github.com/BabylonJS/Babylon.js/blob/master/serializers/src/OBJ/babylon.objSerializer.ts

----
You need to download texture files manually. (to the directory of .OBJ and .MAT files)


Example (mesh is a Mesh with StandardMaterial):


    var obj = BABYLON.OBJExport.OBJ(mesh,true,'birdie');
    var objlink = BABYLON.Tools.FileAsURL(obj);
    var mtl = BABYLON.OBJExport.MTL(mesh,true);
    var mtllink = BABYLON.Tools.FileAsURL(mtl);
    $('#downloadobj A.obj').attr('href',objlink).attr('download','birdie.obj');
    $('#downloadobj A.mtl').attr('href',mtllink).attr('download','birdie.mtl');
    $('#downloadobj').show();
    
