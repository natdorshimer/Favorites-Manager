# cdf
<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/natdorshimer/favorites_module">
    <img src="images\logo.png" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">A PowerShell Directory Favorites Manager<br/></h3>

  <p align="center">
    <a href="https://github.com/natdorshimer/favorites_module"><strong>Explore the docs »</strong></a>
    <br />
    <a href="https://github.com/natdorshimer/favorites_module\issues">Report Bug</a>
    ·
    <a href="https://github.com/natdorshimer/favorites_module/issues">Request Feature</a>
  </p>
</p>

<!-- GETTING STARTED -->
## Getting Started
To use cdf in the PowerShell command line you'll have to add <a href="https://github.com/natdorshimer/favorites_module/blob/master/FavoritesManager/FavoritesManager.psm1">FavoritesManager.psm1</a> to your modules and then import the module in the profile script, ```Microsoft.PowerShell_profile.ps1```

### Installation

1. Download <a href="https://github.com/natdorshimer/favorites_module/blob/master/FavoritesManager/FavoritesManager.psm1">FavoritesManager.psm1</a>

2. Save it to ```\WindowsPowerShell\Modules\FavoritesManager\FavoritesManager.psm1```. This is typically in either ```C:\Users\UserName\Documents\WindowsPowerShell\``` or ```C:\Program Files\WindowsPowerShell\```

## Syntax
    SYNTAX
      cdf [[-alias] <String>] [-add] [-remove] [-path] [-clear] [-list] [-open]
      [<CommonParameters>]
## Parameters
    -alias <String>
        The name of the favorite you wish to perform a command on.

    -add [<SwitchParameter>]
        Switch for adding the selected alias (or name of current directory if none
        is selected) to the favorites list

    -remove [<SwitchParameter>]
        Switch for removing the selected alias (or name of current dir if none
        selected) from the favs list

    -path [<SwitchParameter>]
        Switch for returning the path that the selected alias points to. This has
        higher priority than -list and nullifies list if selected

    -clear [<SwitchParameter>]
        Clears list of favorites if selected. Asks for user confirmation

    -list [<SwitchParameter>]
        Returns the favorites dictionary if selected. cdf -list is the same thing
        as 'cdf' if no other commands are used

    -open [<SwitchParameter>]
        Opens up favorites.txt in notepad if selected

    <CommonParameters>
        This cmdlet supports the common parameters: Verbose, Debug,
        ErrorAction, ErrorVariable, WarningAction, WarningVariable,
        OutBuffer, PipelineVariable, and OutVariable. For more information, see
        about_CommonParameters (https:/go.microsoft.com/fwlink/?LinkID=113216).

<!-- USAGE EXAMPLES -->
## Usage

_For more examples, type_ ```Get-Help cdf -detailed``` _in PowerShell to see the full documentation_

```sh
PS C:\Users\Natalie\Pictures> cdf

Name                           Value
----                           -----
code                           C:\Users\Natalie\code
Documents                      C:\Users\Natalie\Documents
GD                             C:\Users\Natalie\Google Drive

PS C:\> cdf code
PS C:\Users\Natalie\code>
```

```sh
PS C:\Users\Natalie\Pictures> cdf -add
PS C:\Users\Natalie\Pictures> cdf

Name                           Value
----                           -----
code                           C:\Users\Natalie\code
Documents                      C:\Users\Natalie\Documents
GD                             C:\Users\Natalie\Google Drive
Pictures                       C:\Users\Natalie\Pictures
```

```sh
PS C:\Users\Natalie> cdf GD -remove 
PS C:\Users\Natalie> cdf

Name                           Value
----                           -----
code                           C:\Users\Natalie\code
Documents                      C:\Users\Natalie\Documents
Pictures                       C:\Users\Natalie\Pictures
```



<!-- ROADMAP 
## Roadmap

See the [open issues](https://github.com/github_username/repo_name/issues) for a list of proposed features (and known issues).-->

