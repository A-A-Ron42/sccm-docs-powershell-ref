---
description: Gets a Configuration Manager user's device affinities.
external help file: AdminUI.PS.Collections.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMUserDeviceAffinity
---

# Get-CMUserDeviceAffinity

## SYNOPSIS
Gets a Configuration Manager user's device affinities.

## SYNTAX

### SearchByUserNameMandatory (Default)
```
Get-CMUserDeviceAffinity -UserName <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByDeviceNameMandatory
```
Get-CMUserDeviceAffinity -DeviceName <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByDeviceIdMandatory
```
Get-CMUserDeviceAffinity -DeviceId <Int32[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByUserIdMandatory
```
Get-CMUserDeviceAffinity -UserId <Int32[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMUserDeviceAffinity** cmdlet gets one or more user device affinities in Configuration Manager.

User device affinity in Configuration Manager is a method of associating a user with one or more specified devices.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get a user device affinity by using a user name
```
PS XYZ:\> Get-CMUserDeviceAffinity -UserName "CENTRAL\001D$"
```

This command gets the user device affinity for the user named CENTRAL\001D$.

### Example 2: Get a user device affinity by using a user ID
```
PS XYZ:\> Get-CMUserDeviceAffinity -UserID "2063597981"
```

This command gets the user device affinity for the user that has the ID named 2063597981.

### Example 3: Get a user device affinity by using a device name
```
PS XYZ:\> Get-CMUserDeviceAffinity -DeviceName "CMCEN-DIST02"
```

This command gets the user device affinity for the device named CMCEN-DIST02.

### Example 4: Get a user device affinity by using a device ID
```
PS XYZ:\> Get-CMUserDeviceAffinity -DeviceID "2097152000"
```

This command gets the user device affinity for the device that has the ID 2097152000.

## PARAMETERS

### -DeviceId
Specifies an array of device IDs.

```yaml
Type: Int32[]
Parameter Sets: SearchByDeviceIdMandatory
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Specifies an array of device names.

```yaml
Type: String[]
Parameter Sets: SearchByDeviceNameMandatory
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling
DisableWildcardHandling treats wildcard characters as literal character values. Cannot be combined with **ForceWildcardHandling**.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling
ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Cannot be combined with **DisableWildcardHandling**.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserId
Specifies an array of IDs of the primary users of the devices.

```yaml
Type: Int32[]
Parameter Sets: SearchByUserIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName
Specifies an array of names of the primary users of the devices.

```yaml
Type: String[]
Parameter Sets: SearchByUserNameMandatory
Aliases: UniqueUserName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject[]#SMS_UserMachineRelationship

### IResultObject#SMS_UserMachineRelationship

## NOTES

## RELATED LINKS

[Approve-CMUserDeviceAffinityRequest](Approve-CMUserDeviceAffinityRequest.md)

[Deny-CMUserDeviceAffinityRequest](Deny-CMUserDeviceAffinityRequest.md)

[Get-CMUserDeviceAffinityRequest](Get-CMUserDeviceAffinityRequest.md)

[Import-CMUserDeviceAffinity](Import-CMUserDeviceAffinity.md)


