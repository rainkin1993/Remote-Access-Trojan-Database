# Remote-Access-Trojan-Database 

All samples in this database can only used for research purpose.

# the status of all RAT families including programming language used to write RAT stubs, the debut year of RAT families and source to determine the debut year.

The forth column represents the source based on which we determined the year, which could be divided into 3 types: public online documents, compilation timestamp, and the About description.  For the About information, some RAT developers leave the change logs with timestamp in the About window of RATs' control panels, which is useful to identify the debut year.

|       Name       | Programming language | The debut year | Source to determine the year |
|:----------------:|:--------------------:|:--------------:|:----------------------------:|
|       Sub-7      |        Delphi        |      1999      |    https://bit.ly/2p5xjsh    |
|      Nuclear     |        Delphi        |      2003      |    https://bit.ly/2qMzbGH    |
|     Turkojan     |        Delphi        |      2003      |    https://symc.ly/2qJXfdb   |
|    Poison Ivy    |        MASM32        |      2007      |             About            |
|     DarkComet    |        Delphi        |      2008      |    https://bit.ly/367tAe6    |
|     Spycronic    |        Delphi        |      2010      |     Compilation Timestamp    |
|      Spy-Net     |        Delphi        |      2010      |    https://symc.ly/32N7lYR   |
|     CyberGate    |        Delphi        |      2010      |    https://bit.ly/33Y0NXA    |
|      Xtreme      |        Delphi        |      2010      |    https://bit.ly/2NdavQj    |
|     Imperium     |         .NET         |      2011      |     Compilation Timestamp    |
|     NovaLite     |        Delphi        |      2011      |             About            |
|       NjRAT      |         .NET         |      2012      |    https://bit.ly/2p5HsFl    |
|       D-RAT      |         .NET         |      2012      |     Compilation Timestamp    |
|       Bozok      |        Delphi        |      2012      |    https://bit.ly/2MLPiwL    |
|      Greame      |        Delphi        |      2012      |    https://bit.ly/2PlBhrq    |
|      Frutas      |         JAVA         |      2012      |    https://bit.ly/2p5x40l    |
|      Crimson     |         JAVA         |      2012      |    https://bit.ly/32OkuB5    |
|       jSpy       |         JAVA         |      2012      |    https://bit.ly/2NgAAga    |
| Imminent Monitor |         .NET         |      2013      |    https://bit.ly/2NdGnmL    |
|     NanoCore     |         .NET         |      2013      |    https://bit.ly/2BLna6w    |
|      SpyGate     |         .NET         |      2013      |    https://bit.ly/32SyxFK    |
|     VirusRAT     |         .NET         |      2013      |    https://bit.ly/31RtjZn    |
|      Pandora     |        Delphi        |      2013      |    https://symc.ly/36giQdN   |
|      DH RAT      |        Delphi        |      2013      |    https://bit.ly/31SIG49    |
|     Alusinus     |        Delphi        |      2013      |    https://symc.ly/32O7Cen   |
|      njworm      |     Visual Basic     |      2013      |    https://bit.ly/2BMu2R2    |
|       ucuL       |          C++         |      2013      |    https://bit.ly/2PiXmXl    |
|      Adwind      |         JAVA         |      2013      |    https://bit.ly/366qzef    |
|    BackConnect   |         .NET         |      2014      |     Compilation Timestamp    |
|       BXRAT      |         .NET         |      2014      |     Compilation Timestamp    |
|     CloudNet     |         .NET         |      2014      |    https://bit.ly/2Pkgwwb    |
|       L6RAT      |         .NET         |      2014      |     Compilation Timestamp    |
|       Mega       |         .NET         |      2014      |     Compilation Timestamp    |
|      VanTom      |         .NET         |      2014      |    https://bit.ly/2PkgwfF    |
|       XRAT       |         .NET         |      2014      |    https://bit.ly/31Np94P    |
|      Proton      |         .NET         |      2014      |             About            |
|      Quasar      |         .NET         |      2014      |    https://bit.ly/2p5HeOv    |
|       Orion      |        Delphi        |      2014      |     Compilation Timestamp    |
|      HAKOPS      |     Visual Basic     |      2014      |    https://bit.ly/31NDu1h    |
|      Coringa     |         .NET         |      2015      |    https://bit.ly/344tKRG    |
|       ctOs       |         .NET         |      2015      |     Compilation Timestamp    |
|     KilerRAT     |         .NET         |      2015      |    https://bit.ly/2oj7nZz    |
|       MLRAT      |         .NET         |      2015      |     Compilation Timestamp    |
|        MQ5       |         .NET         |      2015      |     Compilation Timestamp    |
|     Comet RAT    |         .NET         |      2015      |     Compilation Timestamp    |
|       Xena       |        Delphi        |      2015      |    https://bit.ly/2WfyfpS    |
|    Rabbit-Hole   |        Delphi        |      2015      |     Compilation Timestamp    |
|     SkyWyder     |     Visual Basic     |      2015      |    https://bit.ly/2pPMvtw    |
|      Babylon     |          C++         |      2015      |    https://bit.ly/2p5DFI8    |
|       Pupy       |        Python        |      2015      |    https://bit.ly/2BPPLHL    |
|    NingaliNet    |         .NET         |      2016      |             About            |
|      Revenge     |         .NET         |      2016      |    https://bit.ly/31L7Xgf    |
|       Maus       |         JAVA         |      2016      |    https://bit.ly/31L7LO3    |


# Explore possible implementation methods of each function from the above RAT families

| KeyLogger | Descriptions & Key APIs                                                                                                                                                                     |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| K1     | RATs invoke NtUserSetWindowsHookEx to register a callback function into a message hook chain of Windows. The callback function will receive a virtual key code  when victims press the key. |
| K2     | RATs invoke NtUserGetAsyncKeyState in an endless loop to poll every key state.                                                                                                              |
| K3     | RawInput is another channel to get user input. RATs invoke NtUserGetRawInputData to get input when a WM_INPUT message occurs.                                                               |


| RemoteCamera | Descriptions & Key APIs                                                                                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C1     | Leveraging DirectShow to access cameras. The DirectShow is a media-streaming architecture for Microsoft Windows. RATs first invoke CoCreateInstance and CreateClassEnumerator to find the video input device.  Then they invoke several APIs (e.g., SetFiltergraph, SetOutputFileName, etc.) to do some configuration works. Finally, they invoke RenderStream to capture video.                |
| C2     | VFW is another multimedia framework developed by Microsoft that allows Windows to play and encode digital video. RATs first invoke capGetDriverDescription to retrieve information of video input devices, and then invoke capCreateCaptureWindow to create a capture window. Finally,  they invoke SendMessage to send messages to the created window to connect and capture cameras. |

| AudioRecord | Descriptions & Key APIs                                                                                                                                                                                                                                                                                                          |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A1     | Leveraging the built-in Waveform-Audio interface to capture audio.  RATs first invoke waveInOpen to open an audio input device.  Then they invoke waveInPrepareHeader and waveInAddBuffer to prepare buffer blocks for audio data. Finally,  they invoke waveInStart to start capturing audio.                                   |
| A2     | The Media Control Interface (MCI) is another built-in interface which provides standard commands for recording multimedia devices. RATs first invoke mciSendCommand with a MCI_OPEN command to open an audio input device, and then invoke the same API mciSendCommand with another command MCI_RECORD to start audio recording. |

TBC