# aasx-server
Server of I40 .AASX packages accessable by REST, OPC UA and MQTT
AASX Server - based on code of AASX Package Explorer


Use aasxserverwindows for windows desktop
Start AasxServerWindows.exe with switch --help to see switches

Use aasxservercore for other platforms
Please install .NET Core Preview 3
https://dotnet.microsoft.com/download/dotnet-core/3.0
  Runtime 3.0.0-preview3-27503-5
Start "dotnet AasxServerCore.dll" with switch --help to see switches

Server loads all .AASX files in the execution directory
Server can be accessed by REST, OPC UA or MQTT (see console)
Every 5 seconds the next submodel is published by MQTT (see console)

If it runs on a PC as localhost
Access REST on localhost:51310
e.g. http://localhost:51310/server/listaas
e.g. http://localhost:51310/aas/id/complete
e.g. http://localhost:51310/aas/id/submodels/CAD/complete
Access OPC UA on opc.tcp://localhost:51210/UA/SampleServer
