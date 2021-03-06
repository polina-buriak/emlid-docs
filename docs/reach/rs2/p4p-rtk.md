# DJI Phantom RTK and Reach RS2 base integration

This guide describes how to set Reach RS2 as a base for DJI Phantom 4 RTK drone. Such setup enables sending the corrections to the DJI RTK drone family during the flight and make real-time precise georeferencing of photos possible. 

DJI RTK drones are using the NTRIP to receive the corrections, that is why Reach RS2 could become a go-to solution as a base station in this setup. In order to make use of such setup, you will need:

- Reach RS2 acting as base
- DJI Phantom 4 RTK
- Internet access on both devices
- NTRIP credentials for RS2 base and DJI drone

You can make your own NTRIP caster by using the open-source caster providers like RTK2Go. We are using the RTK2Go service in this guide as it is available for every potential user of this setup.

## Registration in RTK2Go

RTK2Go is a free-to-use NTRIP caster provider which enables you to make your own Mount Point under its domain. The service requires a free registration procedure:

- Navigate to the RTK2Go site and choose *"Please register before use"* button:

<p style="text-align:center"><img src="../img/reachrs2/p4p/rtk2go-start.png" style="width: 600px;"/></p>

- Fill in your registration details:

<p style="text-align:center"><img src="../img/reachrs2/p4p/rtk2go-registration.png" style="width: 600px;"/></p>

You will receive a confirmation email with the name of your Mount Point and passwords for base and rovers. RTK2Go allows multiple rovers to be connected to one base station, that is why you can make use of it for many devices. For instance, you can send correction data to other Reach rovers to collect accurate data in the field including placing GCPs.

## Configuring Reach RS2

Reach RS2 acts as a base, sending the corrections via NTRIP service. 

- Place the Reach RS2 onto the tripod and provide it with the clear sky view
- Provide the receiver with an Internet access according to [this guide](../connecting-to-the-internet/)
- Navigate to the Base Mode tab and insert the NTRIP credentials for the base station

<p style="text-align:center"><img src="../img/reachrs2/p4p/rv-base-mode.png" style="width: 800px;"/></p>

## Configuring DJI Phantom 4 RTK

- Open GS RTK
- Select Plan or Fly menu. If you choose Plan, select a planning method
- Open Settings by tapping on 3 dots button at the top right corner
- Go to RTK Settings tab
- In RTK Service Type, choose Custom network RTK and fill in NTRIP credentials form

<p style="text-align:center"><img src="../img/reachrs2/p4p/dji-correction-input.png" style="width: 600px;"/></p>

- Tap Connect button. The "Network RTK server connection successful" will appear:

<p style="text-align:center"><img src="../img/reachrs2/p4p/dji-correction-success.png" style="width: 600px;"/></p>

- Base is successfully connected

<p style="text-align:center"><img src="../img/reachrs2/p4p/dji-sattelites.png" style="width: 600px;"/></p>

!!! note ""

	Phantom shows the base's satellites number only if the RTK solution status is fix.


## Performing the Flight

Once the RS2 and drone are set, you can perform your flight. Provide the Phantom 4 with a clear sky view and proceed to the mission:

<p style="text-align:center"><img src="../img/reachrs2/p4p/dji-flight.png" style="width: 600px;"/></p>

You can check the progress of your flight using the map on the bottom left corner of the UI:

<p style="text-align:center"><img src="../img/reachrs2/p4p/dji-plan.png" style="width: 600px;"/></p>

Once the flight is completed, you can download the precisely geotagged photos and use them to create your orthophotos.


Further reading:

- [How RTK works](../common/tutorials/rtk-introduction)
- [Placing the base](../common/tutorials/placing-the-base/)
- [Placing GCPs in RTK](../common/tutorials/placing-gcps)