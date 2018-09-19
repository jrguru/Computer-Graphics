//SHADER PORTION OF THE CODE

precision highp float; //Set the float type to a high precision float
            
            //uniform vec3 mattColor;
            
            varying vec3 vNormal;  //our Normal Vector
            
            void main()    {
                vec3 mattColor = (normalize(vNormal)+ 1.2)/2.0;
                gl_FragColor = vec4(mattColor,1.0);  //returning the global pixel color
            }
             
 

       
//OBJECT THAT WE WILL APPLY THE SHADER TO
 var x, y, z, max = 1.0,min = 0.1,points = [];
                for (var i = 0; i <= 10; i++) {
                    x = Math.floor(Math.random() * (max - min + 1)) + min;
                    y = Math.floor(Math.random() * (max - min + 1)) + min;
                    z = Math.floor(Math.random() * (max - min + 1)) + min;
                    points.push(new THREE.Vector3(x, y, z));
                }
                
                var geometry = new THREE.ConvexGeometry( points );
                

Vertex Shader is defined on Line: 14
Vertex Shader Uniforms Defined: Lines 20, 21, 22
Fragment Shader is defined on Line: 33
Mesh using the Shaders Applied on Lines: 126, 127

