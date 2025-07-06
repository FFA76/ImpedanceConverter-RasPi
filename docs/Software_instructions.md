# Software instructions for Data acquisition

The readout software is the [PhyPiDAQ](https://github.com/PhyPiDAQ) software developed under the direction of Prof. Dr. Guenter Quast for the readout, visualization, and analysis of measurement data from a wide variety of sensors for the Raspberry Pi.

Instructions for installing and getting started with the software can be found at [Installation](https://github.com/PhyPiDAQ/PhyPiDAQ), [Software Description](https://github.com/PhyPiDAQ/PhyPiDAQ/blob/main/docs/Documentation_en.md) and for beginners especially at [Educators Guide](https://github.com/PhyPiDAQ/EducatorsGuide/blob/main/EducatorsGuide.md).
The photoelectric effect experiment is also described in the [PhyPiDAQ](https://github.com/PhyPiDAQ/EducatorsGuide/blob/main/experiments/photoeffect.md) GitHub repository.

In addition to the measuring box and the external setup consisting of the optical setup of the lenses and filters, the photocell and the Hg-lamp, only a capacitor with a size of 1 to 10 nF is required to run the experiment.

To start a series of measurements, all you need to do is adjust the configuration files of the PhypIDAQ software, as shown in the following two code examples.

*photoeffekt.daq:*
```yaml
DeviceFile: config/photoeffekt_ADS1115Config.yaml   # 16 bit ADC, I2C bus
ChanLabels: ['Voltage']            # names for channels 
ChanUnits: ['V']         # units for channels 
ChanColors: [darkblue]      # channel colours in display

Interval: 0.05                 # logging interval  
NHistoryPoints: 20000          # number of points used in history buffer, time=NHistoryPoints*Interval = 2000*0.05 = 100 seconds
DisplayModule: DataGraphs     # text, bar-graph, history and xy-view
Title: "Data from File"       # display title
DataFile:   null              #  null to disable 
CSVseparator: '   '            # field separator, set to ';' for German Excel   
```

*photoeffekt_ADS1115Config.yaml:*
```yaml
DAQModule: ADS1115Config  
ADCChannels: [0]
DifModeChan: [true] # differntial measurement of channel 0 minus 1
Gain: [1]
sampleRate: 860 #max. sample rate
```
Now the measurement can bes started and the charging curve of the capacitor can be displayed and saved as a .csv file.
The results of the measurement series with different wavelengths due to the interference filter can be seen below.

*Fig. 1*: Charging curves of 4.7 nF capacitor for different wave lengths  
                    ![Figure 1](images/curves.png)