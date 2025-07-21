# gRPC
gRPC Advance Actions &amp; Sample Neoload project.                                                                                                                                                               
gRPC is a high performance open source RPC framework introduced by google to facilitate communication between distributed system & micro services. We developed a set of advance actions in Neoload to support gRPC protocol. These advance action will take care of serialization/deserialization of data sending across as well.

## Overview

This repository contains NeoLoad Advanced Actions that allows performance testers using NeoLoad to connect to server & make gRPC calls, both unaray & streaming .
Implementation is in progress.

| Property           | Value                                                                         |
|--------------------|-------------------------------------------------------------------------------|
| Maturity           | Experimental                                                                  |
| Support            | Supported by Neotys                                                           |
| Author             | Neotys                                                                        |
| License            | [BSD Simplified](https://www.neotys.com/gRPCuments/legal/bsd-neotys.txt)       |
| NeoLoad            | 2024.2 (Enterprise or Professional Edition w/ Integration & Advanced Usage)    |
| Bundled in NeoLoad | No                                                                          |
| Download Binaries  | See the [latest release]() |


## Installation

### Setting up the NeoLoad Advance action for SAP RFC

1. Download the latest Advance Action jar [latest release](https://github.com/vijeshv/sap-gRPC/releases/tag/sapgRPC_0.0.1).
   Keept the Jar file in the extlib folder of yor Neoload Project

3. Download the External Refereces files from floder (https://github.com/Neotys-Labs/SAP_RFC/tree/main/ExternalReferences)
   keep Jar files in the extlib folder of yor Neoload Project
   keep the protoc-30.0-win64 file in custom-resources folder of your project

4. restart neoload
## Advanced Actions definitions
## gRPC Connect - Parameters
This Advanced Action helps you to register at gateway as partner, listen for  outbound gRPCS from source system, receive & save in local HDD
| Name                     | Description       |
| ---------------          | ----------------- |
| Connection               | gRPC Channel Name |
| Host                     | gRPC Server name or IP address to connect |
| Port                     | port used for communication|
| SSL                      | SSL coonection or not |


## gRPC InvokeUnary - Parameters
This Advanced Action helps you define tRFC connection to SAP gateway

| Name                     | Description       |
| ---------------          | ----------------- |
| Connection               | gRPC Channel Name |
| Protofile                | Proto file Name with physical path |
| Servicename              | service name in teh format <package.servicename> |
| Method Name              | Name of teh unary method to invoke |
| Data                     | request data in jsonformat |
| Timeout                  | gRPC call timeout. value '0' indicate no timeoutclient will waite as long as server alive and responding |


## gRPC ClientStreaming - Parameters
This Advanced Action helps you simulate Inbound gRPC based on Inbound-gRPC payload template & outbound gRPCS received -Inputs & Oupputs parameters
| Name                     | Description       |
| ---------------          | ----------------- |
| Connection               | gRPC Channel Name |
| Protofile                | Proto file Name with physical path |
| Servicename              | service name in teh format <package.servicename> |
| Method Name              | Name of teh unary method to invoke |
| Datafilepath             | streaming request data (json) file in .txt format |
| Timeout                  | gRPC call timeout. value '0' indicate no timeoutclient will waite as long as server alive and responding |
## gRPC SynchServerStreaming - Parameters
This Advanced Action helps you simulate Inbound gRPC based on Inbound-gRPC payload template & outbound gRPCS received -Inputs & Oupputs parameters
| Name                     | Description       |
| ---------------          | ----------------- |
| Connection               | gRPC Channel Name |
| Protofile                | Proto file Name with physical path |
| Servicename              | service name in teh format <package.servicename> |
| Method Name              | Name of teh unary method to invoke |
| Data                     | request data in jsonformat |
| Timeout                  | gRPC call timeout. value '0' indicate no timeoutclient will waite as long as server alive and responding |
## gRPC AssynchServerStreaming - Parameters
This Advanced Action helps you simulate Inbound gRPC based on Inbound-gRPC payload template & outbound gRPCS received -Inputs & Oupputs parameters
| Name                     | Description       |
| ---------------          | ----------------- |
| Connection               | gRPC Channel Name |
| Protofile                | Proto file Name with physical path |
| Servicename              | service name in teh format <package.servicename> |
| Method Name              | Name of teh unary method to invoke |
| Data                     | request data in jsonformat |
| Timeout                  | gRPC call timeout. value '0' indicate no timeoutclient will waite as long as server alive and responding |
## gRPC BidirectionalStreaming - Parameters(TBD)
This Advanced Action helps you simulate Inbound gRPC based on Inbound-gRPC payload template & outbound gRPCS received -Inputs & Oupputs parameters
| Name                     | Description       |
| ---------------          | ----------------- |
| Destination              | A name of the SAP connection. this name will be using in rest of the actions            |
| template_filepath        | Path of inboud payload template |
| template_filename        | Inbound-Template xml file name |
| parseXML                 | Whether to parse xml for varaible or not|
| responding to Outbound   | whether to scan outbound file received for variable |
| Outbound file directory  | Oubound file directory  at listener side |

Status Codes:
* NL-gRPC_ERROR :  Any gRPC error 

