---
external help file: sharepoint.xml
online version: http://technet.microsoft.com/EN-US/library/7017b7ca-b8b5-4735-a5a8-d12c820dc0a6(Office.15).aspx
schema: 2.0.0
---

# Remove-SPEnterpriseSearchCrawlContentSource

## SYNOPSIS
Deletes a specified crawl content source from a search application.

## SYNTAX

```
Remove-SPEnterpriseSearchCrawlContentSource [-Identity] <ContentSourcePipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 [-SearchApplication <SearchServiceApplicationPipeBind>] [-WhatIf]
```

## DESCRIPTION
The Remove-SPEnterpriseSearchCrawlContentSource cmdlet deletes a specified crawl content source from a service application.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### ------------------EXAMPLE------------------ (SharePoint Server 2013)
```
$searchapp = Get-SPEnterpriseSearchServiceApplication "SearchApp1"

Remove-SPEnterpriseSearchCrawlContentSource -SearchApplication $searchapp -Identity <name>
```

This example retrieves the search service application and deletes a content source.

### ------------------EXAMPLE------------------ (SharePoint Server 2016)
```
C:\PS>$searchapp = Get-SPEnterpriseSearchServiceApplication "SearchApp1"
$topo = Get-SPEnterpriseSearchCrawlTopology -SearchApplication $searchapp
New-SPEnterpriseSearchCrawlTopology -SearchApplication $searchapp -clone -CrawlTopology $topo
$newtopo = Get-SPEnterpriseSearchCrawlTopology -SearchApplication $searchapp -Identity 11111111-1111-1111-1111-111111111111
$cc = Get-SPEnterpriseSearchCrawlComponent -CrawlTopology $newtopo -Identity 22222222-2222-2222-2222-222222222222
$cc | Remove-SPEnterpriseSearchCrawlComponent
$newtopo | Set-SPEnterpriseSearchCrawlTopology -Active
```

This example creates a new, inactive, crawl topology, removes a crawl component from it, and activates the new crawl topology.

## PARAMETERS

### -Identity
The crawl content source to delete.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a ContentSource object (for example, ContentSource1); or an instance of a valid ContentSource object.

```yaml
Type: ContentSourcePipeBind
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AssignmentCollection
Manages objects for the purpose of proper disposal.
Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management.
Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory.
When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.

When the Global parameter is used, all objects are contained in the global store.
If objects are not immediately used, or disposed of by using the Stop-SPAssignment command, an out-of-memory scenario can occur.

```yaml
Type: SPAssignmentCollection
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before executing the command.
For more information, type the following command: get-help about_commonparameters

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchApplication
Specifies the search application that contains the crawl content source.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid SearchServiceApplication object.

```yaml
Type: SearchServiceApplicationPipeBind
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Displays a message that describes the effect of the command instead of executing the command.
For more information, type the following command: get-help about_commonparameters

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Online Version](http://technet.microsoft.com/EN-US/library/7017b7ca-b8b5-4735-a5a8-d12c820dc0a6(Office.15).aspx)
