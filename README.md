[index.html](https://github.com/user-attachments/files/28258040/index.html)
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>AR Lanzaguisantes Animado</title>
  
  <script src="https://aframe.io/releases/1.5.0/aframe.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/mind-ar@1.2.5/dist/mindar-image-aframe.prod.js"></script>
  
  <script src="https://cdn.jsdelivr.net/gh/c-frame/aframe-extras@7.2.0/dist/aframe-extras.min.js"></script>

  <style>
    body { margin: 0; overflow: hidden; }
  </style>
</head>
<body>

  <a-scene 
    mindar-image="imageTargetSrc: ./models/targets.mind;" 
    color-space="sRGB" 
    renderer="colorManagement: true, physicallyCorrectLights: true" 
    embedded 
    vr-mode-ui="enabled: false" 
    device-orientation-permission-ui="enabled: false">
    
    <a-assets>
      <a-asset-item id="modeloLanzaguisantes" src="./models/mi_personaje.glb"></a-asset-item>
    </a-assets>

    <a-camera position="0 0 0" look-controls="enabled: false"></a-camera>
    
    <a-entity mindar-image-target="targetIndex: 0">
      
      <a-gltf-model 
        src="#modeloLanzaguisantes" 
        scale="0.1 0.1 0.1" 
        position="0 0 0" 
        rotation="0 0 0"
        animation-mixer>
      </a-gltf-model>

    </a-entity>
  </a-scene>

</body>
</html>
