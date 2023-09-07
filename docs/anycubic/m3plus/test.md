<h1 style="font-size:1.5vw"><span style="color:black">M3 PLUS</span></h1>

The Anycubic Photon M3 Plus is part of the new M3 line by Anycubic, positioned as the middle child. However, don't be mistaken by its designation, as this printer boasts several standout features. With a large build volume and a 6K Mono LCD, it can handle printing large-sized objects with high resolution and impressive speed, curing each layer in just 1.5 seconds. Notably, the M3 Plus includes an automatic resin vat filling system, the option for a camera to monitor prints, and Wi-Fi connectivity through Anycubic's Cloud ecosystem. This printer offers a range of functionalities while maintaining a compact and lightweight design, making it a popular choice in the prosumer market.
<br>

[Anycubic](https://www.anycubic.com/products/photon-m3-plus)
<br>

[Review](https://3dprinterly.com/simple-anycubic-photon-m3-plus-review-worth-buying-or-not/)


<br>

# Material(Resin) parameters 

| Detection project                | Detection method                                                         | Rigid110              |
|----------------------------------|--------------------------------------------------------------------------|-----------------------|
| Colour                           |                                                                          | White/Bleu/Grey/Black |
| Viscosity (30°C)                 |                                                                          | 402mPa.s              |
| Density (25°C)                   |                                                                          | 1.13g/ml              |
| Tensile strength (MPa)           | ASTM D638M                                                               | 42.7                  |
| Tensile module (MPa)             | ASTM D638M                                                               | 2900                  |
| Elongation at break(%)           | ASTM D638M                                                               | 33.1                  |
| Bending strength (MPa)           | ASTM D790                                                                | 77.4                  |
| Flexural modulus (MPa)           | ASTM D790                                                                | 1674.1                |
| Impact strength (J/m)            | ASTM D256                                                                | 39.3                  |
| Water absorption (%)             | ASTM D570                                                                | 0.43                  |
| Shore hardness (D)               | ASTM D2241                                                               | 85                    |
| Heat distortion temperature (°C) | Simple method                                                            | 65                    |
| Shrinkage(%)                     | Measurement of dimensional expansion and contraction in the XY direction | X:-0.24%;Y:-0.24%     |
|                                  |                                                                          |                       |
<br>

![](https://cdn.jsdelivr.net/gh/yannickkabasso/Profabx-images/img/Screenshot%202023-09-07%20155712.png)

<br>

# Support parameters (default) 

| Z Lift Hight    | Support script | Support angle      | Anchor distance     | Border anchor distance | Border offset      | No support offset | Lowest anchor distance | Reinforce height  |
| --------------- | -------------- | ------------------ | ------------------- | ---------------------- | ------------------ | ----------------- | ---------------------- | ----------------- |
| 10mm            | Medium         | 45°                | 3mm                 | 2mm                    | 0.5mm              | 2mm               | 1.5mm                  | 1.5mm             |
| Polygon edge N° | Max branch N°  | Branch top width   | Branch bottom width | Trunk top width        | Trunk bottom width | Trunk height      | Branch max angle       | Distance in model |
| 6               | 2              | 1mm                | 1.2mm               | 1.2mm                  | 1.5mm              | Branch max angle  | 45°                    | 0.3mm             |
| Length          | Tip type       | Break point height | Break point width   | Start height           | End height         | Exposure time(s)  |Max branch number|Branch max angle  |
|2mm|perpendicular to surface|0.1mm|0.2mm|0.1mm|0.1mm|5  |   4                 |45° 

<br>

# TEST1: Top Width
The top width of supports in the realm of 3D printing is defined as the width (D) of the contact point where the support structure interfaces with the lower surface of the model being printed. This dimension plays a critical role in determining the level of stability and support provided to the model during the printing process. By adjusting the top width, users can regulate the extent of contact between the support structure and the model, thereby influencing factors such as ease of removal post-printing and the overall quality of the final result. It is worth noting that finding the optimal top width requires careful consideration of various factors, including the complexity of the model, the material being used, and the specific requirements of the intended application. As such, striking the right balance between support effectiveness and ease of post-processing is essential to achieving successful 3D prints.
<br>

| Date/Cube |  Top width |Anycubic photon workshop   | Printed model | Remark | 
| --------- | ---------- | ------------------------- | ------------- | -------|
| 0821/V1   |  0.2mm     |  <img src="https://cdn.jsdelivr.net/gh/yannickkabasso/Profabx-images/img/0821M1.png" alt="drawing" width="300"/>  |<img src="https://cdn.jsdelivr.net/gh/yannickkabasso/Profabx-images/img/M1.png" alt="drawing" width="300"/>|When employing the default parameters as mentioned earlier, specifically a top width of 0.2mm for support structures, it becomes evident that the bottom surface exhibits a noticeable bend, and the supports do not establish the intended connection with the model (Cube) as anticipated. This issue arises from the observed disparity between the printed results and the desired outcome.|          
| 0821/v2   |          0.4mm     |<img src="https://cdn.jsdelivr.net/gh/yannickkabasso/Profabx-images/img/0821M2.png" alt="drawing" width="300"/> | <img src="https://cdn.jsdelivr.net/gh/yannickkabasso/Profabx-images/img/M2.png" alt="drawing" width="300"/>   |Upon modifying the top width of the support structures to 0.4mm, a marginal improvement is discernible on the bottom surface. However, it remains bent, failing to achieve the desired flatness. Furthermore, despite this alteration, the supports continue to exhibit a lack of proper connection with the intended model (Cube)   
| 0821/v3   |           0.6mm     |<img src="https://cdn.jsdelivr.net/gh/yannickkabasso/Profabx-images/img/0821M3.png" alt="drawing" width="300"/>  |<img src="https://cdn.jsdelivr.net/gh/yannickkabasso/Profabx-images/img/M3.jpg" alt="drawing" width="300"/>                 |Upon modifying the top width of the support structures to 0.6mm, a marginal improvement is discernible on the bottom surface. However, it remains bent, failing to achieve the desired flatness. Furthermore, despite this alteration, the supports continue to exhibit a lack of proper connection with the intended model (Cube)         
| 0821/v4   |          0.8mm     |<img src="https://cdn.jsdelivr.net/gh/yannickkabasso/Profabx-images/img/0821M4.png" alt="drawing" width="300"/>  |<img src="https://cdn.jsdelivr.net/gh/yannickkabasso/Profabx-images/img/M4.jpg" alt="drawing" width="300"/>                  |Upon modifying the top width of the support structures to 0.8mm, a marginal improvement is discernible on the bottom surface. However, it remains bent, failing to achieve the desired flatness. Furthermore, despite this alteration, the supports continue to exhibit a lack of proper connection with the intended model (Cube)       
| 0821/v5   |          1mm       |<img src="https://cdn.jsdelivr.net/gh/yannickkabasso/Profabx-images/img/0821M5.png" alt="drawing" width="300"/>  |<img src="https://cdn.jsdelivr.net/gh/yannickkabasso/Profabx-images/img/M5.jpg" alt="drawing" width="300"/>               |Best result:<br>Upon modifying the top width of the support structures to 1mm, it becomes evident that a marginal improvement is discernible on the bottom surface close to a flat surface. However, it remains a little bent, failing to achieve the desired flatness. Furthermore, despite this alteration, some of the supports continue to exhibit a lack of proper connection with the intended surface of the cube, deviating from the anticipated outcome. Consequently, additional adjustments or alternative strategies may be required to rectify these persistent issues and attain the desired printing results. 

