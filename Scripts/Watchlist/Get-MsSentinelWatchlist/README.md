# Get-MsSentinelWatchlist
The "Get-MsSentinelWatchlist.ps1" 📄 file is a PowerShell script designed to list all watchlists in Microsoft Sentinel. Here is a breakdown of its functionality:

***Purpose***: Lists all watchlists in Microsoft Sentinel.

***Dependencies***: 
- Requires Powershell 5 (or above).
- Requires the Az.Accounts module.

***Usage Example***: 

`Get-MsSentinelWatchlist -WorkspaceName 'MyWorkspace'`

`Get-MsSentinelWatchlist -WorkspaceName 'MyWorkspace' -Verbose`

## Parameters
- ***WorkspaceName***(string): The name of the Azure workspace (mandatory).

## Functionality
- ***Azure Connection***:
    - Retrieves the current Azure context. If not connected, it prompts the user to connect using device authentication.
    - Outputs the subscription ID to confirm the connection.

- ***Workspace Retrieval***:
    - Retrieves the specified Azure workspace.
    - Constructs the API path for accessing watchlists if the workspace exists.

- ***Watchlist Retrieval***:
    - Uses Invoke-AzRestMethod to fetch watchlists from the constructed API path.
    - If successful, it processes the response to list all watchlists.
    - Error handling is in place to provide feedback if the watchlists cannot be retrieved.

## Result
<img src="https://github.com/Warfion/Sentinel/blob/main/Scripts/Watchlist/Get-MsSentinelWatchlist/image/image.png">
<img src="https://github.com/Warfion/Sentinel/blob/main/Scripts/Watchlist/Get-MsSentinelWatchlist/image/image_1.png">

## Links:
https://learn.microsoft.com/en-us/rest/api/securityinsights/watchlists/list?view=rest-securityinsights-2024-03-01&tabs=HTTP
                             
Created by: Thomas Bruend
