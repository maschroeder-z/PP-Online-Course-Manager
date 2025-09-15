# Online Learning Course Manager

## Summary

Provides an Power Platform Canvas App to mange learning courses. Managed course offers, allows people to register to courses. The App managed the available seats, offers a course filter and includes an Power Automate Flow to notify participants about course changes. The App creates on demand an appointment entry in the user calendar.
 
![Start screen with no selected course](assets/screen-01.png)
*Start screen with no selected course*

![Selected course with all details](assets/screen-02.png)
*Selected course with all details*

![Filter for courses](assets/screen-03.png)
*Filter for courses.*

![Show only courses for the current user](assets/screen-04.png)
*Show only courses for the current user.*

![E-Mail Notification about course changes](assets/screen-05.png)

*E-Mail Notification about course changes*

## Applies to
![Power Apps](https://img.shields.io/badge/Power%20Apps-Yes-green "Yes")
![Power Automate](https://img.shields.io/badge/Power%20Automate-Yes-green "Yes")
![Power BI](https://img.shields.io/badge/Power%20BI-No-red "No")
![Power Pages](https://img.shields.io/badge/Power%20Pages-No-red "No")
![Power Virtual Agents](https://img.shields.io/badge/Power%20Virtual%20Agents-No-red "No")
![Dataverse](https://img.shields.io/badge/Dataverse-No-red "No")
![AI Builder](https://img.shields.io/badge/AI%20Builder-No-red "No")
![Custom Connectors](https://img.shields.io/badge/Custom%20Connectors-No-red "No")
![Power Fx](https://img.shields.io/badge/Power%20Fx-Yes-green "Yes")

## Compatibility

<!--
Update the compatibility below.

If a premium license is not required and there are no experimental features used in your solution:
![Premium License](https://img.shields.io/badge/Premium%20License-Not%20Required-red.svg "Premium license not required")
![Experimental Features](https://img.shields.io/badge/Experimental%20Features-No-red.svg "Does not rely on experimental features")

If a premium license is required and there are experimental features used in your solution:
![Premium License](https://img.shields.io/badge/Premium%20License-Required-green.svg "Premium license required")
![Experimental Features](https://img.shields.io/badge/Experimental%20Features-Yes-green.svg "Does rely on experimental features")

Don't worry if you're unsure about the compatibility matrix above. We'll verify it when we approve the PR. 
-->

![Premium License](https://img.shields.io/badge/Premium%20License-Not%20Required-red.svg "Premium license not required")
![Experimental Features](https://img.shields.io/badge/Experimental%20Features-No-red.svg "Does not rely on experimental features")

## Contributors
<!--
We use this section to recognize and promote your contributions. Please provide one author per line -- even if you worked together on it.

We'll only use the info you provided here. Make sure to include your full name, not just your GitHub username.

Provide a link to your GitHub profile to help others find more cool things you have done. The only link we'll accept is a link to your GitHub profile.

If you want to provide links to your social media, blog, and employer name, make sure to update your GitHub profile.
-->

* Marc Andre Schröder-Zhou (https://github.com/maschroeder-z)

## Version history

Version|Date|Comments
-------|----|--------
1.0|September 15, 2025|Initial release

## Prerequisites
The Canvas App uses SharePoint Custom lists to store and manage all information. The solution uses enviroment variables to define the concrete URL addresses for the lists.
Following lists are needed:
* List with all Trainings
* List to save registered user
* List for external trainer data (used as lookup list)
Alle lists can be created with the JSON-file from the Lists directory with the PnP-command Add-PnPSiteScript. 
![List form for manage course data](assets/screen-06.png)
*List form for manage course data*

## Minimal path to awesome

<!-- 
PRO TIP:

For commands, use the `code syntax`

For button labels, page names, dialog names, etc. as they appear on the screen, use **Bold**

Don't use "click", use "select" or "use"

As tempting as it may be, don't just use images to describe the steps. Let's be as inclusive as possible and think about accessibility.

-->

### Using the solution zip

* [Download](./dist/Schulungsverwaltung_1_0_0_1.zip) the `.zip` from the `solution` folder
* Within **Power Apps Studio**, import the solution `.zip` file using **Solutions** > **Import Solution** and select the `.zip` file you just packed.
* During installation set the enviroment variables to your lists
* Open the app in edit mode and make sure the data source **Data source name** is connected correctly.

### Using the source code

You can also use the [Power Apps CLI](https://docs.microsoft.com/powerapps/developer/data-platform/powerapps-cli) to pack the source code by following these steps:

* Clone the repository to a local drive
* Pack the source files back into a solution `.zip` file:

  ```bash
  pac solution pack --zipfile pathtodestinationfile --folder pathtosourcefolder --processCanvasApps
  ```

  Making sure to replace `pathtosourcefolder` to point to the path to this sample's `sources` folder, and `pathtodestinationfile` to point to the path of this solution's `.zip` file (located under the `dist` folder)
* Within **Power Apps Studio**, import the solution `.zip` file using **Solutions** > **Import Solution** and select the `.zip` file you just packed.

## Features
This solution illustrates the following concepts on top of the Power Platform:
* Use always query delegation. Prevent loading of huge amount of data.
* Use advanced filtering.
* Use additional connector to create appointment entries in user calendar.
* Combined with an Power Automate Flow in one solution

## Video
[![SharePoint Online & Power Plattform: interne Weiterbildung – einfach, digital, effizient](https://img.youtube.com/vi/eqonr-PNE6E/hqdefault.jpg)](https://youtu.be/eqonr-PNE6E)

## Help
Please contact me for further help or information about the sample.

## Disclaimer

**THIS CODE IS PROVIDED *AS IS* WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**

<img src="https://m365-visitor-stats.azurewebsites.net/powerplatform-samples/samples/YOUR-SOLUTION-NAME"  aria-hidden="true" />
