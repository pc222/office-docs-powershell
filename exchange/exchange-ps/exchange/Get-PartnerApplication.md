---
applicable: Exchange Server 2013, Exchange Server 2016, Exchange Online
schema: 2.0.0
---

# Get-PartnerApplication

## SYNOPSIS
This cmdlet is available in on-premises Exchange and in the cloud-based service. Some parameters and settings may be exclusive to one environment or the other.

Use the Get-PartnerApplication cmdlet to retrieve settings for a partner application.

For information about the parameter sets in the Syntax section below, see Exchange cmdlet syntax (https://technet.microsoft.com/library/bb123552.aspx).

## SYNTAX

```
Get-PartnerApplication [[-Identity] <PartnerApplicationIdParameter>] [-DomainController <Fqdn>]
 [-Organization <OrganizationIdParameter>] [<CommonParameters>]
```

## DESCRIPTION
!!! Exchange Server 2013

In Microsoft Exchange Server 2013, you can configure partner applications such as Microsoft SharePoint to access Exchange resources. For details, see Integration with SharePoint and Lync.

You need to be assigned permissions before you can run this cmdlet. Although all parameters for this cmdlet are listed in this topic, you may not have access to some parameters if they're not included in the permissions assigned to you. To see what permissions you need, see the "Partner applications - configure" entry in the Sharing and collaboration permissions topic.

!!! Exchange Server 2016, Exchange Online

You can configure partner applications such as Microsoft SharePoint to access Exchange resources. For details, see Plan Exchange 2016 integration with SharePoint and Skype for Business.

You need to be assigned permissions before you can run this cmdlet. Although this topic lists all parameters for the cmdlet, you may not have access to some parameters if they're not included in the permissions assigned to you. To find the permissions required to run any cmdlet or parameter in your organization, see Find the permissions required to run any Exchange cmdlet (https://technet.microsoft.com/library/mt432940.aspx).

## EXAMPLES

### Example 1 -------------------------- (Exchange Server 2013)
```
Get-PartnerApplication | Format-List *
```

This example retrieves settings for all partner applications configured in Exchange and pipes them to the Format-List cmdlet to display all properties in a list view.

### Example 1 -------------------------- (Exchange Server 2016)
```
Get-PartnerApplication | Format-List *
```

This example retrieves settings for all partner applications configured in Exchange and pipes them to the Format-List cmdlet to display all properties in a list view.

### Example 1 -------------------------- (Exchange Online)
```
Get-PartnerApplication | Format-List *
```

This example retrieves settings for all partner applications configured in Exchange and pipes them to the Format-List cmdlet to display all properties in a list view.

## PARAMETERS

### -DomainController
This parameter is available only in on-premises Exchange.

The DomainController parameter specifies the domain controller that's used by this cmdlet to read data from or write data to Active Directory. You identify the domain controller by its fully qualified domain name (FQDN). For example, dc01.contoso.com.

```yaml
Type: Fqdn
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity
The Identity parameter specifies the identity of a partner application.

```yaml
Type: PartnerApplicationIdParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: 1
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### -Organization
!!! Exchange Server 2013

The Organization parameter is reserved for internal Microsoft use.



!!! Exchange Server 2016, Exchange Online

This parameter is reserved for internal Microsoft use.



```yaml
Type: OrganizationIdParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

###  
To see the input types that this cmdlet accepts, see Cmdlet Input and Output Types (https://go.microsoft.com/fwlink/p/?linkId=616387). If the Input Type field for a cmdlet is blank, the cmdlet doesn't accept input data.

## OUTPUTS

###  
To see the return types, which are also known as output types, that this cmdlet accepts, see Cmdlet Input and Output Types (https://go.microsoft.com/fwlink/p/?linkId=616387). If the Output Type field is blank, the cmdlet doesn't return data.

## NOTES

## RELATED LINKS

[Online Version](https://technet.microsoft.com/library/e6ce8128-f174-4bca-91e6-004fc94cf0f8.aspx)

