# Show List "Label" Instead of "Value" in XSLT Report

This sample shows a way to get and display "Labels" in Reports by customizing Stylesheet of Report item. Normally Reports show "values" of differrent Fields/Properties.

## History

This project and the following release notes have been migrated from the old Aras Projects page.

Release | Notes
--------|--------
[v2.0.0](https://github.com/ArasLabs/list-label-xslt-sample/releases/tag/v2.0.0) | Verified on 11.0 SP12, 15; Upgraded Method & Report code to support current open release (11.0 SP12)
[v1](https://github.com/ArasLabs/list-label-xslt-sample/releases/tag/v1) | Initial Release

#### Supported Aras Versions

Project | Aras
--------|------
[v2.0.0](https://github.com/ArasLabs/list-label-xslt-sample/releases/tag/v2.0.0) | 10.0+, 11.0+
[v1](https://github.com/ArasLabs/list-label-xslt-sample/releases/tag/v1) | 9.2.0

## Installation

#### Important!
**Always back up your code tree and database before applying an import package or code tree patch!**

### Pre-requisites

1. Aras Innovator installed
2. Aras Package Import tool
3. **SampleForLabelsInReports** import package

### Install Steps

1. Backup your database and store the BAK file in a safe place.
2. Open up the Aras Package Import tool.
3. Enter your login credentials and click **Login**
  * _Note: You must login as root for the package import to succeed!_
4. Enter the package name in the TargetRelease field.
  * Optional: Enter a description in the Description field.
5. Enter the path to your local `..\SampleForLabelsInReports\Import\imports.mf` file in the Manifest File field.
6. Select all in the Available for Import field.
7. Select Type = **Merge** and Mode = **Thorough Mode**.
8. Click **Import** in the top left corner.
9. Close the Aras Package Import tool.
10. Login to Aras as admin.
11. Navigate to **Administration > ItemTypes** in the TOC. 
12. Search for the Part ItemType and open for editing. 
13. In the Reports tab of the Part ItemType select **Pick Related**, and then click **New Relationship** icon next to it. 
14. In the resulting Dialog Box search and select **Part Report With Label**, and then click **Return Selected icon** (checkmark icon). 
15. Save, unlock, and close the Part ItemType.

## Usage

![Example Screenshot](./Screenshots/Report-screenshot-2.png)
Note: Make/Buy Labels altered for Demo purposes in the above.

1. Login to Aras.
2. Navigate to **Design > Parts**. 
3. Create a few Parts. Make sure to select either Make or Buy in the Make/Buy field.
4. Run a Search to display the items just created.
5. From the Menu at the top, select **Reports > Part Report With Label**. This will run the report and display results similar to the screen capture file included with this package.

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request

## Credits

Created by Aras Corporation Support.

## License

Published to Github under the MIT license. See the [LICENSE file](./LICENSE.md) for license rights and limitations.
