---
applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016
schema: 2.0.0
---

# Get-RpcClientAccess

## SYNOPSIS
!!! Exchange Server 2010

Use the Get-RpcClientAccess cmdlet to display the settings for the Exchange RPC Client Access service that's running on the Client Access server role on Microsoft Exchange Server 2010.

!!! Exchange Server 2013

This cmdlet is available only in on-premises Exchange.

Use the Get-RpcClientAccess cmdlet to display the settings for the Exchange RPC Client Access service that's running on a Microsoft Exchange server.

For information about the parameter sets in the Syntax section below, see Exchange cmdlet syntax (https://technet.microsoft.com/library/bb123552.aspx).

!!! Exchange Server 2016

This cmdlet is available only in on-premises Exchange.

Use the Get-RpcClientAccess cmdlet to view the settings of the Microsoft Exchange RPC Client Access service on Exchange servers that have the Client Access server role installed. These settings affect Outlook clients that connect by using Outlook Anywhere (RPC over HTTP).

For information about the parameter sets in the Syntax section below, see Exchange cmdlet syntax (https://technet.microsoft.com/library/bb123552.aspx).

## SYNTAX

```
Get-RpcClientAccess [-DomainController <Fqdn>] [-Server <ServerIdParameter>] [<CommonParameters>]
```

## DESCRIPTION
!!! Exchange Server 2010

The Get-RpcClientAccess cmdlet returns the Exchange RPC Client Access service configuration for Exchange Client Access servers. Information can be returned only about servers located in the Exchange organization from which the cmdlet is run.

You need to be assigned permissions before you can run this cmdlet. Although all parameters for this cmdlet are listed in this topic, you may not have access to some parameters if they're not included in the permissions assigned to you. To see what permissions you need, see the "RPC Client Access settings" entry in the Client Access Permissions topic.

!!! Exchange Server 2013

The Get-RpcClientAccess cmdlet returns the Exchange RPC Client Access service configuration for Exchange servers. Information can be returned only about servers located in the Exchange organization from which the cmdlet is run.

You need to be assigned permissions before you can run this cmdlet. Although all parameters for this cmdlet are listed in this topic, you may not have access to some parameters if they're not included in the permissions assigned to you. To see what permissions you need, see the "RPC Client Access settings" entry in the Clients and mobile devices permissions topic.

!!! Exchange Server 2016

You need to be assigned permissions before you can run this cmdlet. Although this topic lists all parameters for the cmdlet, you may not have access to some parameters if they're not included in the permissions assigned to you. To find the permissions required to run any cmdlet or parameter in your organization, see Find the permissions required to run any Exchange cmdlet (https://technet.microsoft.com/library/mt432940.aspx).

## EXAMPLES

### Example 1 -------------------------- (Exchange Server 2010)
```
Get-RpcClientAccess -Server CAS01
```

This example displays the parameters and values for the Client Access server CAS01 that's running the Exchange RPC Client Access service.

### Example 1 -------------------------- (Exchange Server 2013)
```
Get-RpcClientAccess -Server ENT01
```

This example displays the parameters and values for the Exchange server ENT01 that's running the Exchange RPC Client Access service.

### Example 1 -------------------------- (Exchange Server 2016)
```
Get-RpcClientAccess
```

This example displays a summary list of the RPC Client Access service settings on all the servers in the organization.

### Example 2 -------------------------- (Exchange Server 2016)
```
Get-RpcClientAccess -Server ENT01 | Format-List
```

This example returns detailed information for the RPC Client Access service on the server named ENT01.

## PARAMETERS

### -DomainController
The DomainController parameter specifies the domain controller that's used by this cmdlet to read data from or write data to Active Directory. You identify the domain controller by its fully qualified domain name (FQDN). For example, dc01.contoso.com.

```yaml
Type: Fqdn
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Server
!!! Exchange Server 2010

The Server parameter specifies the Client Access server.



!!! Exchange Server 2013

The Server parameter specifies the Exchange server.



!!! Exchange Server 2016

The Server parameter specifies the Exchange server that you want to view.

You can use any value that uniquely identifies the server. For example:

- Name (for example, Exchange01)

- Distinguished name (DN) (for example, CN=Exchange01,CN=Servers,CN=Exchange Administrative Group (FYDIBOHF23SPDLT),CN=Administrative Groups,CN=First Organization,CN=Microsoft Exchange,CN=Services,CN=Configuration,DC=contoso,DC=com)

- Exchange Legacy DN (for example, /o=First Organization/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Configuration/cn=Servers/cn=Exchange01)

- GUID (for example, bc014a0d-1509-4ecc-b569-f077eec54942)



```yaml
Type: ServerIdParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016

Required: False
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

###  
To see the input types that this cmdlet accepts, see Cmdlet Input and Output Types (https://go.microsoft.com/fwlink/p/?LinkId=616387). If the Input Type field for a cmdlet is blank, the cmdlet doesn't accept input data.

## OUTPUTS

###  
To see the return types, which are also known as output types, that this cmdlet accepts, see Cmdlet Input and Output Types (https://go.microsoft.com/fwlink/p/?LinkId=616387). If the Output Type field is blank, the cmdlet doesn't return data.

## NOTES

## RELATED LINKS

[Online Version](https://technet.microsoft.com/library/3462fe0b-929d-4106-840e-99d7d1e12f40.aspx)

