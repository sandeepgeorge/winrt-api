---
-api-id: P:Windows.Networking.NetworkOperators.MobileBroadbandCellUmts.LocationAreaCode
-api-type: winrt property
---

<!-- Property syntax.
public IReference<uint> LocationAreaCode { get; }
-->

# Windows.Networking.NetworkOperators.MobileBroadbandCellUmts.LocationAreaCode

## -description
Gets the Location Area Code (LAC).

> [!NOTE]
> This functionality is only available to mobile operator apps and Windows Store apps given privileged access by mobile network operators.

> If you want to use this API and publish your app to the Store, you will need special approval. For more information, see the **Special and restricted capabilities** section under [App capability declarations](https://docs.microsoft.com/en-us/windows/uwp/packaging/app-capability-declarations). 

## -property-value
The Location Area Code (LAC).

## -remarks
The range of this value is 0~65535; returns null if unknown.

## -see-also

## -examples


## -capabilities
cellularDeviceIdentity, cellularDeviceControl
