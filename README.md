### CDR (Call Detail Record) Decoder for Ericsson, Siemens D900 MSC [^1] 

[^1]: Automatically exported from [code.google.com/p/cdr-decoder](https://code.google.com/archive/p/cdr-decoder/)

This project includes the following components:

##### CDR.Decoder.Core.dll

.Net 2.0 library. Contains all functions to work with ASN.1 CDR-files, work with:
- Siemens D900 MSC - versions SR13 (CS-50) and earlier (CS-10) [SiemensD900.CDR.Definition.xml];
- Ericsson - SEQUENCE OF UMTSGSMPLMNCallDataRecord [Ericsson.CDR.Definition.xml];
- Ericsson Gateway GPRS Support Node (GGSN) [Ericsson_GGSN.CDR.Definition.xml];
- Ericsson Serving GPRS Support Node R7 (SGSN R7) [Ericsson_SGSN_R7.CDR.Definition.xml].

Sample CDR.Decoder.Core.dll.config:
```
 <?xml version="1.0" encoding="utf-8" ?> <XMLDefinitionFile>Ericsson_GGSN.CDR.Definition.xml</XMLDefinitionFile>
```

##### CDR.Decoder.exe

.Net 2.0 Windows Forms application. Decoding CDR-file with the record results in the log-file

Usage:
```
CDR.Decoder.exe [/s]

/s - Autorun decoding process. In the end of the decoding process, the program will return result-code.

If the next argument - is the name of CDR-file, the decoder will create a new task with the settings by default to decode the file.

/d: - Specify the directory that contains the CDR-files. You can use wildcards "." and "?" in path-string.

/j: - Load the saved job settings.
```

