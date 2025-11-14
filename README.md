<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <title>Mi Primer Programa de Realidad Virtual (con Sofá)</title>
    <meta name="description" content="A-Frame Hello World VR.">
    <script src="https://aframe.io/releases/1.5.0/aframe.min.js"></script>
    <style>
        body { margin: 0; overflow: hidden; }
        .a-enter-vr-button {
            background-color: #0d6efd !important;
        }
    </style>
</head>
<body>
    <a-scene>
        <a-sky color="#ADD8E6"></a-sky> 

        <a-plane position="0 0 -4" rotation="-90 0 0" width="10" height="10" color="#7BC8A4" shadow></a-plane>

        <a-plane position="0 2.5 -9" width="10" height="5" color="#D3D3D3" shadow></a-plane>

        <a-box position="-3 1.5 -3" rotation="0 45 0" color="#FF0000" shadow></a-box>

        <a-sphere position="3 1.2 -5" radius="0.8" color="#4CC3D9" shadow>
            <a-animation attribute="rotation"
                         dur="5000"
                         from="0 0 0"
                         to="0 360 0"
                         repeat="indefinite">
            </a-animation>
        </a-sphere>

        <a-entity 
            gltf-model="url(https://cdn.glitch.com/c67f01e7-24ef-4b44-a957-30e4871d8ad2%2Fsofamoderno.glb?v=1614710170138)"
            position="0 0 -5"  
            rotation="0 180 0" 
            scale="2 2 2"      
            shadow>
        </a-entity>
        <a-entity camera look-controls wasd-controls position="0 1.6 0"></a-entity> 
        
        <a-entity light="type: ambient; color: #BBB"></a-entity>
        <a-entity light="type: directional; color: #FFF; intensity: 0.6" position="-1 1 2"></a-entity>
        <a-entity light="type: point; intensity: 0.4; distance: 10" position="0 3 -4"></a-entity>

    </a-scene>
</body>
</html>
