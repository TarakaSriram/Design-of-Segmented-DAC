# Design-of- 8 bit Segmented-Digital to Analog Converter

A segmented DAC employs multiple individual DAC sub-circuits, also known as segments, to collectively generate a more accurate and finely-tuned analog output. Each segment of the DAC corresponds to a specific range or portion of the digital input code, and these segments are often combined to achieve higher precision and improved linearity in the analog output. Because this the overall performance, including DNL, will be improved.

So if we want to implement higher bit say 32 bit in this passion, we need higher value of the resistor i.e 2^31 , so that's the constraint of area.So we move onto anthor archeitecture R-2R ladder.


An R-2R DAC, also known as a Digital-to-Analog Converter, employs a pair of accurate resistors to transform a digital binary code into an analog output signal that varies in relation to the numerical magnitude of the binary input. Here, resistor values remain the same even for higher bits.

So here DNL is used as a metric/parameter in order to find the performance of the DAC. DNL, or Differential Nonlinearity, is a critical parameter in the context of digital-to-analog converters (DACs). It measures the deviation between the ideal step size of the DAC output and the actual step size observed in real-world performance. In other words, DNL quantifies the accuracy of the DAC's transitions between adjacent output levels.

A DNL value of 0 indicates perfect linearity, meaning each step in the digital input corresponds exactly to an expected step in the analog output. Positive DNL values suggest that the output step is larger than desired, while negative DNL values imply that the output step is smaller than expected.

In practical terms, DNL impacts the precision and integrity of the analog signal produced by the DAC. High DNL values can result in nonuniform spacing between output levels, causing distortion and inaccuracies in the converted analog signal. Therefore, minimizing DNL is crucial for achieving high-quality, accurate analog outputs in digital-to-analog converters. DNL is meaasured in terms of LSB.

When DAC is completly implemented with the R-2R , then DNL will not be that great as expected from the ideal behaviour, so in order to get the better performance a new type of archeitecture is being imlemented that is called segmented DAC, here i have implemented 8 bit Segmented DAC. In which first 5 bits are implemeted in R-2R structure and the last 3 bits are implemented in binary weighted form.

A segmented DAC  employs multiple individual DAC sub-circuits, also known as segments, to collectively generate a more accurate and finely-tuned analog output. Each segment of the DAC corresponds to a specific range or portion of the digital input code, and these segments are often combined to achieve higher precision and improved linearity in the analog output. Because which the overall performance including DNL will be improved.
