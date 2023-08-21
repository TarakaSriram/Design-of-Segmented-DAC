# Design-of- 8 bit Segmented-Digital to Analog Converter
![image](https://github.com/TarakaSriram/Design-of-Segmented-Digital-to-Analog-Converter/assets/65438040/71f31470-5468-404d-8477-fcd1dedbb1aa)

The 4 bit binary weighted DAC

A 4-bit binary number has 16 combinations (0000 to 1111) represented by A, B, C, D. Doubling bit weights yields 8-4-2-1 binary code (2^3, 2^2, 2^1, 2^0). With D=1kΩ, C=2kΩ, B=4kΩ, A=8kΩ, and RF=1kΩ, the 4-bit binary weighted DAC's transfer characteristic is formed as 
![image](https://github.com/TarakaSriram/Design-of-Segmented-Digital-to-Analog-Converter/assets/65438040/04f6ceba-5d2a-4661-8bc6-cfb6bfc795a3)

So if we want to implement higher bit say 32 bit in this passion, we need higher value of the resistor i.e 2^31 , so that's the constraint of area.So we move onto anthor archeitecture R-2R ladder.

![image](https://github.com/TarakaSriram/Design-of-Segmented-Digital-to-Analog-Converter/assets/65438040/7a720e13-ed8a-4910-8289-810f649b4d30)

An R-2R DAC, also known as a Digital-to-Analog Converter, employs a pair of accurate resistors to transform a digital binary code into an analog output signal that varies in relation to the numerical magnitude of the binary input. Here resistor values remain the same even for higher bits also.

So here DNL is used as metric/parameter inorder to find the performance of the DAC. DNL, or Differential Nonlinearity, is a critical parameter in the context of digital-to-analog converters (DACs). It measures the deviation between the ideal step size of the DAC output and the actual step size observed in real-world performance. In other words, DNL quantifies the accuracy of the DAC's transitions between adjacent output levels.

A DNL value of 0 indicates perfect linearity, meaning each step in the digital input corresponds exactly to an expected step in the analog output. Positive DNL values suggest that the output step is larger than desired, while negative DNL values imply that the output step is smaller than expected.

In practical terms, DNL impacts the precision and integrity of the analog signal produced by the DAC. High DNL values can result in nonuniform spacing between output levels, causing distortion and inaccuracies in the converted analog signal. Therefore, minimizing DNL is crucial for achieving high-quality, accurate analog outputs in digital-to-analog converters. DNL is meaasured in terms of LSB.

When DAC is completly implemented with the R-2R , then DNL will not be that great as expected from the ideal behaviour, so in order to get the better performance a new type of archeitecture is being imlemented that is called segmented DAC, here i have implemented 8 bit Segmented DAC. In which first 5 bits are implemeted in R-2R structure and the last 3 bits are implemented in binary weighted form.

A segmented DAC  employs multiple individual DAC sub-circuits, also known as segments, to collectively generate a more accurate and finely-tuned analog output. Each segment of the DAC corresponds to a specific range or portion of the digital input code, and these segments are often combined to achieve higher precision and improved linearity in the analog output. Because which the overall performance including DNL will be improved.
