## Developer Guide 

# Customization Tool Reference 

# 2025 R1 


<!-- PAGE_BREAK -->
 Contents | 2 

## Contents 

 Copyright...............................................................................................................................................4 

 Access Rights......................................................................................................................................... 5 

 Analytical Reports.................................................................................................................................. 7 

 Actions.................................................................................................................................................. 9 

 ASPX Editor.......................................................................................................................................... 22 

 Business Events.................................................................................................................................... 23 

 Code.................................................................................................................................................... 25 

 Code Editor.......................................................................................................................................... 27 

 Conditions............................................................................................................................................29 

 Connected Applications.........................................................................................................................33 

 Custom Files.........................................................................................................................................35 

 Custom Files (Modern UI)...................................................................................................................... 38 

 Customization Menu............................................................................................................................. 40 

 Customization Project Editor................................................................................................................. 43 

 Customization Projects......................................................................................................................... 48 

 Customized Data Classes....................................................................................................................... 54 

 Customized Screens.............................................................................................................................. 56 

 Data Class............................................................................................................................................ 58 

 Database Scripts...................................................................................................................................64 

 Dashboards.......................................................................................................................................... 68 

 Dialog Boxes.........................................................................................................................................70 

 Edit Project Items................................................................................................................................. 74 

 Element Inspector................................................................................................................................ 76 

 Event Handlers..................................................................................................................................... 78 

 Fields...................................................................................................................................................82 

 Generic Inquiries.................................................................................................................................. 86 

 Import and Export Scenarios................................................................................................................. 88 

 Mobile Application................................................................................................................................ 90 

 Mobile Workspaces............................................................................................................................... 93 

 Modern UI Editor.................................................................................................................................. 95 

 Project XML Editor................................................................................................................................ 96 

 Push Notifications................................................................................................................................ 97 

 Reports................................................................................................................................................ 99 

 Screen Editor......................................................................................................................................101 


<!-- PAGE_BREAK -->
 Contents | 3 

**Shared Filters..................................................................................................................................... 106** 

**Site Map............................................................................................................................................. 108** 

**Source Code....................................................................................................................................... 110** 

**System Locales................................................................................................................................... 113** 

**Tables to Track Deleted Records...........................................................................................................115** 

**User-Defined Fields............................................................................................................................. 117** 

**Webhooks...........................................................................................................................................119** 

**Web Service Endpoints........................................................................................................................ 121** 

**Wikis.................................................................................................................................................. 123** 

**Workflow (Diagram View).................................................................................................................... 125** 

**Workflow (Tree View).......................................................................................................................... 136** 

**Workflows.......................................................................................................................................... 147** 


<!-- PAGE_BREAK -->
 Copyright | 4 

## Copyright 

**©** (^) **2025 Acumatica, Inc. ALL RIGHTS RESERVED.** No part of this document may be reproduced, copied, or transmitted without the express prior consent of Acumatica, Inc. 3075 112th Avenue NE, Suite 200, Bellevue, WA 98004, USA 

### Restricted Rights 

 The product is provided with restricted rights. Use, duplication, or disclosure by the United States Government is subject to restrictions as set forth in the applicable License and Services Agreement and in subparagraph (c)(1)(ii) of the Rights in Technical Data and Computer Soware clause at DFARS 252.227-7013 or subparagraphs (c)(1) and (c)(2) of the Commercial Computer Soware-Restricted Rights at 48 CFR 52.227-19, as applicable. 

### Disclaimer 

 Acumatica, Inc. makes no representations or warranties with respect to the contents or use of this document, and specifically disclaims any express or implied warranties of merchantability or fitness for any particular purpose. Further, Acumatica, Inc. reserves the right to revise this document and make changes in its content at any time, without obligation to notify any person or entity of such revisions or changes. 

### Trademarks 

 Acumatica is a registered trademark of Acumatica, Inc. HubSpot is a registered trademark of HubSpot, Inc. Microso Exchange and Microso Exchange Server are registered trademarks of Microso Corporation. All other product names and services herein are trademarks or service marks of their respective companies. 

 Soware Version: 2025 R1 

 Last Updated: 06/01/2025 


<!-- PAGE_BREAK -->
 Access Rights | 5 

## Access Rights 

 Page ID: (AU205200) 

 On this page, you manage the ScreenWithRights items in the customization project. A ScreenWithRights item contains the dataset of the custom access rights of roles to a form, down to the control of form elements. 

 You open the Access Rights page by clicking Access Rights in the navigation pane of the Customization Project Editor. 

### Page Toolbar and More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Command Description 

 Manage Access Rights 

 Opens the Access Rights by Screen (SM201020) form in a new browser tab, so that you can specify the access rights of the screen that was selected in the table. 

 Reload from Database 

 Updates the ScreenWithRights items in the customization project if these items have been modified on the forms related to user access configuration, such as Access Rights by Screen (SM201020), Access Rights by Role (SM201025), and Access Rights by User (SM201055). 

 Table: Add Access Rights for Screen Dialog Box This dialog box opens when you click Add New Record on the page toolbar. The dialog box contains the following elements. 

 Element Description 

 The dialog box contains the following elements. 

 Screen ID The ID of the form for which the access rights will be added. In the lookup box, you can type the name or ID of the form to quickly locate it. 

 Merge Rule A group of option buttons indicating the way the system applies the access rights from the customization project when publishing it. You select one of the following option buttons: 

- **Grant All** : To set the access rights to _Granted_ for all user roles in the system 

- **Revoke All** : To set the access rights to _Revoked_ for all user roles in the system 

- **Apply and Reset** : To apply the access rights from the customization project and set     them to _Revoked_ for the roles that are not included in the customization project 

- **Apply and Keep** (default): To apply the access rights from the customization project     and keep them unchanged for the roles that are not included in the customization     project 

 This dialog box has the following buttons. 


<!-- PAGE_BREAK -->
 Access Rights | 6 

 Element Description 

 Add Adds the selected access rights to the table on the page and closes the dialog box. 

 Cancel Closes the dialog box without making any changes. 

### Table 

 This table lists the ScreenWithRights items in the customization project. The columns of the table are described below. 

 Column Description 

 Object Name The ID of the form for which the access rights will be added. 

 Description The description of the access rights. 

 Merge Rule A group of option buttons indicating the way the system applies the access rights from the customization project when publishing it. The following options are available: 

- _Grant All_ : To set the access rights to _Granted_ for all user roles in the system 

- _Revoke All_ : To set the access rights to _Revoked_ for all user roles in the system 

- _Apply and Reset_ : To apply the access rights from the customization project and set     them to _Revoked_ for the roles that are not included in the customization project 

- _Apply and Keep_ (default): To apply the access rights from the customization project     and keep them unchanged for the roles that are not included in the customization     project For details, see _To Add Access Rights to a Project_. 

 Last Modified By The name of the user who last modified the access rights in the customization project. 

 Last Modified On The date when the access rights were last modified in the customization project. 


<!-- PAGE_BREAK -->
 Analytical Reports | 7 

## Analytical Reports 

 Page ID: (AU206003) 

 On this page, you manage the ReportDefinition items in the customization project. A ReportDefinition item contains the dataset of a custom analytical report, including the data of a predefined set of rows, columns, and units. 

 You open the Analytical Reports page by clicking Analytical Reports in the navigation pane of the Customization Project Editor. 

### Page Toolbar and More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Command Description 

 Manage Report Definitions 

 Opens the Report Definitions (CS206000) form in a new browser tab. 

 Reload from Database 

 Updates the ReportDefinition items in the customization project if the analytical reports that correspond to these items have been modified on the Report Definitions form. 

 Table: Add Report Definition Dialog Box This dialog box opens when you click Add New Record on the page toolbar. The dialog box contains a table with the following elements. 

 Element Description 

 The table toolbar includes only standard buttons. For the list of standard buttons, see Table Toolbar. 

 The table in the dialog box has the following columns. 

 Included A check box that indicates (if selected) that the current report will be added to the customization project if you click Save. 

 Code The internal name of the report. 

 Description The description of the report. 

 Last Modified By The name of the user who last modified the report in the customization project. 

 Last Modified On The date when the report was last modified in the customization project. 

 This dialog box has the following buttons. 

 Save Adds the selected report to the table on the page and closes the dialog box. 

 Cancel Closes the dialog box without making or saving any changes. 


<!-- PAGE_BREAK -->
 Analytical Reports | 8 

### Table 

 This table contains a list of the analytical reports that have been modified in the customization project. The columns of the table are described below. 

 Column Description 

 Object Name The name of the report in the customization project. 

 Description The description of the report. 

 Last Modified By The name of the user who last modified the report in the customization project. 

 Last Modified On The date when the report was last modified in the customization project. 


<!-- PAGE_BREAK -->
 Actions | 9 

## Actions 

 Page ID: (AU201050) 

 For a particular screen (that is, a form in Acumatica ERP), you use this page to add a new action, modify an action in a predefined workflow, or modify an action defined in a graph. 

 The table on the page displays actions added in the predefined workflow and actions added in previous versions of Acumatica ERP. 

 You open the Actions page by clicking Actions under the screen ID (of the form for which you are adding or modifying actions) in the navigation pane of the Customization Project Editor. In the name that appears on the page, Actions is preceded by the form ID and then the form name in parentheses. 

### Page Toolbar and More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Command Description 

 Add Existing Action Opens the Action Properties dialog box, in which you can select an existing action, modify its properties (if needed), and then add this action to the workflow. 

 Create New Action Opens the Action Properties dialog box, where you can specify the settings of a new action. 

 This is a standard toolbar button that you use to add a new record on most pages. 

 Delete Row Deletes the action selected in the table. You click the row with the action before you click this button. 

 Manage Categories Opens the Manage Categories dialog box. In this dialog box, you can reorder the categories on the More menu of the Acumatica ERP form (that is, the screen) whose actions you are viewing, change the names of existing categories, and add new categories. 

 Reorder Actions Opens the Reorder Actions dialog box, where you can reorder the actions located on the form toolbar of the Acumatica ERP form (that is, the screen for which you have opened the Actions page), or in a selected category of the More menu of this form. 

 Reverse Change Opens the Reverse Change dialog box, in which you can click OK to return all actions to their predefined state. 


<!-- PAGE_BREAK -->
 Actions | 10 

 Command Description 

 View Changes Opens the Changes dialog box, where you can view the description of an action in JSON format. If any changes have been applied to a predefined action, they are highlighted in the dialog box. You can return the action to its predefined state by clicking Reverse Change in the Changes dialog box. 

 The View Changes command is available only if the action is inherited—that is, based on a predefined action. 

### Action Properties Dialog Box 

 This dialog box opens when you click Create New Action on the page toolbar or Add Existing Action on the More menu, or when you click the link with the action name in the table on the page. 

 Table: Action Properties Dialog Box: Summary Area The Summary area of this dialog box has the following elements. 

 Element Description 

 Action Name The internal name of the action. 

 This box is read-only if you have opened the dialog box by clicking the link with the action name in the table on the page. 

 Display Name The name of the action that will be displayed on the Acumatica ERP form that corresponds to the screen. 

 Disabled An indicator of when the action is disabled. 

 By default, the box is empty, indicating that the action is always enabled. If the box is not empty, it can contain one of the following: 

- _True_ : The action is always disabled. 

- Condition: The condition that, if it is met, causes the action to be disabled. If any con-     ditions are specified on the _Conditions_ page for the screen of this action, they are avail-     able for selection in this box. If the action is used in a workflow and its availability depends on the state of the applica- ble entity, you need to specify this property in this state. 

 This box does not appear in the dialog box if the action has the Navigation: Side Panel type. 

 Hidden An indicator of when the action is hidden. 

 By default, the box is empty, indicating that the action is always visible. If the box is not empty, it can contain one of the following: 

- _True_ : The action is always hidden. 

- Condition: The condition that, if it is met, causes the action to be hidden. If any condi-     tions are specified on the _Conditions_ page for the screen of this action, they are avail-     able for selection in this box. If the action is used in a workflow and its visibility depends on the state of the applicable entity, you need to specify this property in this state. 

 This box does not appear in the dialog box if the action has the Navigation: Side Panel type. 


<!-- PAGE_BREAK -->
 Actions | 11 

**Element Description** 

**Dialog Box** The dialog box that will be displayed when the action is clicked on the form, if applicable. For details, see _Dialog Boxes_. 

 This box does not appear in the dialog box if the action has the Navigation: Side Panel type. 

**Icon** The icon that will be displayed for the action on the side panel. 

 This box appears only if the action has the Navigation: Side Panel type. 

**Processing Screen** The screen ID of the processing form of Acumatica ERP on which the action will be an option in the **Action** box, in addition to being available on the form for which the action is defined. 

 This box does not appear in the dialog box if the action has the Navigation: Side Panel type. 

 On a mass-processing form, if you add to a schedule a workflow action that invokes a dialog box in which a user should enter some additional information, then for automated processing, the system uses the default values of this dialog box. 

 For details on how to schedule mass processing, see Scheduling Automated Processing. 

**Batch Mode** A check box that (if selected) indicates that the records will be mass-processed on the Acumatica ERP form specified in the **Processing Screen** box. 

 This check box does not appear in the dialog box if the action has the Navigation: Side Panel type. 

**Action Type** The type of the action. 

 You can select one of the following options: 

- _Run Report_ : The action runs the report whose ID is specified in the **Destination Screen**     box. 

- _Navigation: Search Records_ : The action redirects the user to the form whose ID is spec-     ified in the **Destination Screen** box and on which the user can search for records     (such as an inquiry or a generic inquiry). 

- _Navigation: Create Record_ : The action redirects the user to the data entry form whose     ID is specified in the **Destination Screen** box and on which the user can create a     record. 

- _Navigation: Side Panel_ : The action opens as a side panel the form whose ID is speci-     fied in the **Destination Screen** box. With this option selected, you can specify a form     of any of the following types as the destination: dashboard, report, or generic inquiry. 

- _Workflow_ : The action changes the state of an entity as a part of a workflow. 

- _Graph Action:_ Read-only. The action that is defined in a graph. This option is not avail-     able for selection when you are creating an action. This box is read-only if you have opened the dialog box by clicking the link with the action name in the table on the page. 


<!-- PAGE_BREAK -->
 Actions | 12 

**Element Description** 

**Category** The category of the More menu in which the menu command associated with the action will be displayed on the form. The list of categories available for selection depends on the form. To manage the categories, you click **Manage Categories** on the page toolbar. 

 This box does not appear in the dialog box if the action has the Navigation: Side Panel type. 

**Destination Screen** Required. The screen or report that will be opened when the action redirects a user to a different screen. 

 This box does not appear in the dialog box if the action has the Workflow or Graph Action type. 

 Depending on the type of the action, you can specify the screen ID as follows: 

- For the _Run Report_ type: The screen ID of the report that you want to run and to which     you want to redirect the user, such as _Sales Order Summary_ ( _SO610500_ ). 

- For the _Navigation: Search Records_ type: The screen ID of the form to which you want     to redirect the user; this is a form where a user can search for records, such as an in-     quiry or a generic inquiry. For example, you might specify this action type with the     screen ID _SO3010PL_ , which is the ID of the list of records for the Sales Orders entry     form. 

- For the _Navigation: Create Record_ type: The screen ID of the form to which you want     to redirect the user; this is a form on which a user can create a new record. For ex-     ample, you might specify _SO301000_ as the screen ID; it is the ID of the _Sales Orders_     (SO301000) data entry form. 

- For the _Navigation: Side Panel_ type: The screen ID of the form that will be opened in a     side panel when a user clicks the action. You can specify the following types of forms:     dashboards, reports, and generic inquiries. For example, you might specify _AR3030PL_     as the screen ID; it is the ID of the Customers (AR3030PL) list of records. 

**Window Mode** An option that indicates whether the results of the action will be displayed on the same tab, on a new tab, or in a pop-up window. 

 This box does not appear in the dialog box if the action has the Navigation: Side Panel , Workflow , or Graph Action type. 

**Rights to Enable Action** 

 The minimum level of access rights that a user must have for the action to be enabled on the form. The access rights of user roles are specified on the Access Rights by Screen (SM201020) form. 

 If the action has the Workflow type, this option is set to Update by default. This means that for the action to be available on the form, a user must have the Edit access rights for the form. If the action has the Navigation: Search Records , Navigation: Create Record , or Run Report type, this option is set to Select by default. This means that a user must have View Only access rights (or a more permissible level) for the action to be available on the form. 

 This box does not appear in the dialog box if the action has the Navigation: Side Panel type. 

**Rights to View Action** 

 The minimum level of access rights that a user must have for the action to be visible on the form. 

 This box does not appear in the dialog box if the action has the Navigation: Side Panel type. 


<!-- PAGE_BREAK -->
 Actions | 13 

**Element Description** 

**Expose to Mobile** A check box that (if selected) indicates that the action will be available on the corresponding mobile screen. The check box is cleared by default. To expose this action on the mobile screen, you need to select this check box. 

 This box does not appear in the dialog box if the action has the Navigation: Side Panel type. 

**Display on Toolbar** The way the action is displayed on the form toolbar and under a category on the More menu. One of the following options can be selected: 

- _Hide_ : The action will not be displayed on the form toolbar but will be displayed under     a category on the More menu if a category is specified for it. However, if you select the     **Duplicate on Toolbar** check box for this action in a workflow state, the action will be     displayed on the form toolbar when the record is in this state. 

- _If Available_ : The action will be displayed as a button on the form toolbar and under a     category on the More menu if the action is available for a record based on its state and     if a category is specified for it. If the action is available but no category is specified, the     action will be displayed on the form toolbar and under the **Other** category. If the ac-     tion is not available or a record based on its state, it will not be displayed on the form     toolbar and the More menu. 

- _Always_ : The action will be displayed as a button on the form toolbar and under a cat-     egory on the More menu even if the action is unavailable for the record based on its     state. 

- _As Configured in Graph_ : The action will be displayed according to the properties of the     _PXButton_ attribute of the action. 

 This box does not appear in the dialog box if the action has the Navigation: Side Panel type. 

**Connotation** A color notation that gives users additional information. For example, you can use connotations to indicate to users which action in the entity processing workflow is the one most likely to be taken (given the state of the entity), which actions require special consideration, and which actions provide links to additional information, such as reports. 

 On the More menu, the connotation is displayed as a dot of the selected color (see the list below) after the associated menu command. If the action is also displayed on the form toolbar, it is highlighted in the selected color. 

 The possible values and corresponding colors are as follows: 

- _Primary_ : The primary color of the site theme 

- _Secondary_ : The secondary color of the site theme 

- _Success_ : Green 

- _Danger_ : Red 

- _Warning_ : Yellow 

- _Info_ : Blue 

- _Light_ : Light gray 

- _Dark_ : Dark gray This box does not appear in the dialog box if the action has the _Navigation: Side Panel_ type. 


<!-- PAGE_BREAK -->
 Actions | 14 

**_Table: Action Properties Dialog Box: Navigation Parameters Tab_** 

On this tab, you specify the navigation parameters for the action. These parameters depend on the type of action and are the following: 

- For an action of the _Run Report_ type: The parameters of the report 

- For an action of the _Navigation: Search Records_ type: The parameters by which the records are filtered 

- For an action of the _Navigation: Create Records_ type: The values for the fields of the new record 

- For an action of the _Navigation: Side Panel_ type: The parameters that will be passed to the side panel 

The tab is not shown in the dialog box if the action has the _Graph Action_ type. 

The table toolbar includes only standard buttons. For the list of standard buttons, see _Table Toolbar_. 

The columns of the table are described below. 

 Column Description 

 Active A check box that indicates (if selected) that the parameter in this row is active. 

 Parameter Name The name of the parameter. 

 Value The value of the parameter. 

 From Schema A check box that indicates (if selected) that the parameter value from the database should be used. 

**_Table: Action Properties Dialog Box: Field Update Tab_** 

This tab contains a table with the fields whose properties should be modified when the action is performed. 

The tab is not available if the action has the _Navigation: Side Panel_ type. 

The table toolbar includes only standard buttons. For the list of standard buttons, see _Table Toolbar_. 

The columns of the table are described below. 

 Column Description 

 Active A check box that indicates (if selected) that the field should be updated. 

 Field The name of the field that should be updated. 

 From Schema A check box that indicates (if selected) that field value from the database should be used. 

 New Value The new value for the field. 

 Status The status of the field update. 

**_Table: Action Properties Dialog Box: Action Parameters Tab_** 

On this tab, you specify the action parameters that should be applied to the action method. 

The tab is available only if the action has the _Graph Action_ type. 

The table toolbar includes only standard buttons. For the list of standard buttons, see _Table Toolbar_. 

The columns of the table are described below. 


<!-- PAGE_BREAK -->
 Actions | 15 

 Column Description 

 Active A check box that indicates (if selected) that the parameter in this row is active. 

 Parameter Name The name of the action parameter. 

 From Schema A check box that indicates (if selected) that parameter value from the database should be used. 

 Value The value of the action parameter. 

 Status The status of the parameter. 

**_Table: Action Properties Dialog Box: Action Executed on Success Tab_** 

On this tab, you specify the subscriber actions—that is, the actions that the system should execute if the action is executed successfully. 

The table toolbar includes only standard buttons. For the list of standard buttons, see _Table Toolbar_. 

The columns of the table are described below. 

 Column Description 

 Active A check box that indicates (if selected) that the subscriber action in this row is active. 

 Action Name The name of the subscriber action. 

 The lookup table contains all actions except those with the Side Panel type 

 Action Type Read-only. The type of the subscriber action, which can be one of the following: 

- _Run Report_ : The action runs the report whose ID is specified in the **Destination Screen**     box. 

- _Navigation: Search Records_ : The action redirects the user to the form whose ID is spec-     ified in the **Destination Screen** box and on which the user can search for records     (such as an inquiry or a generic inquiry). 

- _Navigation: Create Record_ : The action redirects the user to the data entry form whose     ID is specified in the **Destination Screen** box and on which the user can create a     record. 

- _Navigation: Side Panel_ : The action opens as a side panel the form whose ID is speci-     fied in the **Destination Screen** box You can specify the following types of forms: dash-     boards, reports, and generic inquiries. 

- _Workflow_ : The action changes the state of an entity as a part of a workflow. 

- _Graph Action:_ Read-only. The action that is defined in a graph. This option is not avail-     able for selection when you are creating an action. 

 Execution Condition 

 The condition that (if fulfilled) makes the system execute the subscriber. 

 The default value of this column is True , which indicates that the system always executes the subscriber. You can select another condition, if needed. 


<!-- PAGE_BREAK -->
 Actions | 16 

 Column Description 

 Dialog Box Read-only. The dialog box that is specified for the action in the workflow. When the system executes the action, the system does not display this dialog box to the user; instead, the system uses the dialog box values specified on the Dialog Boxes page. 

 The name of the dialog box is a link that you can click to open the Dialog Box Values dialog box. 

 Stop on Error A check box that indicates (if selected) that the system will not execute the subsequent subscriber actions if the current subscriber (the subscriber in this row) has failed. 

 Status Read-only. The status of the subscriber action, which can be one of the following: 

- _New_ : A subscriber action that you have added 

- _Modified_ : A system subscriber action that you have modified 

- _Inherited_ : A system subscriber action 

**_Table: Action Properties Dialog Box: Triggering Actions Tab_** 

On this tab, you can view and add triggering actions—that is, actions that trigger the execution of the action. 

The table toolbar includes only standard buttons. For the list of standard buttons, see _Table Toolbar_. 

The columns of the table are described below. 

 Column Description 

 Active A check box that indicates (if selected) that the triggering action in this row is active. 

 Action Name The name of the triggering action. The lookup table contains all actions except those with the Side Panel type. 

 This box is filled in automatically if you have added the action as a subscriber. 

 Action Type Read-only. The type of the triggering action, which can be one of the following: 

- _Run Report_ : The action runs the report whose ID is specified in the **Destination Screen**     box. 

- _Navigation: Search Records_ : The action redirects the user to the form whose ID is spec-     ified in the **Destination Screen** box and on which the user can search for records     (such as an inquiry or a generic inquiry). 

- _Navigation: Create Record_ : The action redirects the user to the data entry form whose     ID is specified in the **Destination Screen** box and on which the user can create a     record. 

- _Navigation: Side Panel_ : The action opens as a side panel the form whose ID is speci-     fied in the **Destination Screen** box You can specify the following types of forms: dash-     boards, reports, and generic inquiries. 

- _Workflow_ : The action changes the state of an entity as a part of a workflow. 

- _Graph Action:_ Read-only. The action that is defined in a graph. This option is not avail-     able for selection when you are creating an action. 

 Execution Condition 

 The condition that (if fulfilled) makes the system execute the current action. 

 The default value of this column is True , which indicates that the system always executes the current action. You can select another condition, if needed. 


<!-- PAGE_BREAK -->
 Actions | 17 

 Column Description 

 Dialog Box Read-only. The dialog box that is specified for the current action in the workflow. When the system executes the action, the system does not display this dialog box to the user; instead, the system uses the dialog box values specified on the Dialog Boxes page. 

 The name of the dialog box is a link that you can click to open the Dialog Box Values dialog box. 

 Stop on Error A check box that indicates (if selected) that the system will stop the execution of subsequent actions if the current action (the one in this row) fails. 

 Status Read-only. The status of the triggering action, which can be one of the following: 

- _New_ : A triggering action that you have added 

- _Modified_ : A system triggering action that you have modified 

- _Inherited_ : A system triggering action 

 Table: Action Properties Dialog Box: Buttons The dialog box includes the following buttons. 

 Button Description 

 OK Closes the dialog box and applies the changes. 

 Cancel Closes the dialog box without making any changes. 

### Manage Categories Dialog Box 

 This dialog box opens when you click Manage Categories on the page toolbar. In this dialog box, you can change the order of the existing categories on the More menu of the form you are modifying. If needed, you can also add new categories. 

 Element Description 

 The table toolbar includes standard buttons and buttons that are specific to this table. For the list of standard buttons, see Table Toolbar. The table-specific buttons are listed below. 

 Add Category Opens the New Category dialog box, where you can add a new category. 

 Move Up Moves the selected row up, which causes the selected category to be moved up on the More menu. You click the row you want to move before clicking this button. 

 Move Down Moves the row down, which causes the selected category to be moved down on the More menu. You click the row you want to move before clicking this button. 

 The table contains the following columns. 

 Category Name The internal name of the category. 

 Display Name The name of the category that will be displayed on the More menu of the form. 

 This dialog box has the following buttons. 


<!-- PAGE_BREAK -->
 Actions | 18 

 Element Description 

 OK Closes the dialog box and applies the changes. 

 Cancel Closes the dialog box without saving any changes. 

### New Category Dialog Box 

 This dialog box opens when you click Add Category on the table toolbar of the Manage Categories dialog box. In the dialog box, you can add a new category to the More menu of the form whose actions you are modifying. 

 Element Description 

 The dialog box has the following elements. 

 Category Name The internal name of the category. 

 Display Name The name of the category that will be displayed on the More menu of the form. 

 This dialog box has the following buttons. 

 OK Closes the dialog box and applies the changes. 

 Cancel Closes the dialog box without making any changes. 

### Reorder Actions Dialog Box 

 This dialog box opens when you click Reorder Actions on the More menu. In the dialog box, you can change the position of the action in the category of the More menu where it is listed. 

 Element Description 

 The Summary area contains the following element. 

 Category The list of categories on the More menu in which the menu command associated with the action is displayed. 

 The table toolbar includes standard buttons and buttons that are specific to this table. For the list of standard buttons, see Table Toolbar. The table-specific buttons are listed below. 

 Move Up Moves up the row, which causes the selected action to be moved up in the category of the More menu. 

 Move Down Moves down the row, which causes the selected action to be moved down in the category of the More menu. 

 The table contains the following elements. 

 Action Name The internal name of the action. 

 Display Name The name of the action that will be displayed on the applicable Acumatica ERP form. 


<!-- PAGE_BREAK -->
 Actions | 19 

 Element Description 

 Action Type The type of the action, which is one of the following: 

- _Run Report_ : The action runs the report whose ID is specified in the **Destination Screen**     box. 

- _Navigation: Search Records_ : The action redirects the user to the form whose ID is spec-     ified in the **Destination Screen** box and on which the user can search for records     (such as an inquiry or a generic inquiry). 

- _Navigation: Create Record_ : The action redirects the user to the data entry form whose     ID is specified in the **Destination Screen** box and on which the user can create a     record. 

- _Navigation: Side Panel_ : The action opens as a side panel the form whose ID is speci-     fied in the **Destination Screen** box You can specify the following types of forms: dash-     boards, reports, and generic inquiries. 

- _Workflow_ : The action changes the state of an entity as a part of a workflow. 

- _Graph Action:_ Read-only. The action that is defined in a graph. This option is not avail-     able for selection when you are creating an action. 

 This dialog box has the following buttons. 

 OK Closes the dialog box and applies the changes. 

 Cancel Closes the dialog box without applying any changes. 

### Changes Dialog Box 

 You use this dialog box to view the source code of the action; the changes are highlighted in red. The dialog box also contains the following buttons. 

 Button Description 

 Reverse Change Returns the action to its predefined state. 

 Close Closes the dialog box. 

### Table 

 This table contains the list of actions and the basic settings of each of them. When you click the link in the Action Name column, the Action Properties dialog box is opened. The columns of the table are described below. 

 Table: Table Columns 

 Column Description 

 Action Name The internal name of the action. When you click the name, the Action Properties dialog box is opened, which shows the properties of the selected action. 

 Display Name The name of the action that will be displayed on the applicable Acumatica ERP form. 


<!-- PAGE_BREAK -->
 Actions | 20 

**Column Description** 

**Action Type** The type of the action. 

 This column can contain one of the following options: 

- _Run Report_ : The action runs the report whose ID is specified in the **Destination Screen**     box. 

- _Navigation: Search Records_ : The action redirects the user to the form whose ID is spec-     ified in the **Destination Screen** box and on which the user can search for records     (such as an inquiry or a generic inquiry). 

- _Navigation: Create Record_ : The action redirects the user to the data entry form whose     ID is specified in the **Destination Screen** box and on which the user can create a     record. 

- _Navigation: Side Panel_ : The action opens as a side panel the form whose ID is specified     in the **Destination Screen** box. If this option is selected, you can specify a form of any     of the following types as the destination: dashboard, report, or generic inquiry. 

- _Workflow_ : The action changes the state of an entity as a part of a workflow. 

- _Graph Action:_ Read-only. The action that is defined in a graph. This option is not avail-     able for selection when you create an action. 

**Disabled** An indicator of when the action is disabled. 

 By default, the column is empty, indicating that the action is always enabled. If the column is not empty, it can contain one of the following: 

- _True_ : The action is always disabled. 

- Condition: The condition that, if it is met, causes the action to be disabled. If any con-     ditions are specified on the _Conditions_ page for the screen that contains this action,     they are available for selection in this column. 

**Hidden** An indicator of when the action is hidden. 

 By default, the column is empty, indicating that the action is always visible. If the column is not empty, it can contain one of the following: 

- _True_ : The action is always hidden. 

- Condition: The condition that, if it is met, causes the action to be hidden. If any condi-     tions are specified on the _Conditions_ page for the screen that contains this action, they     are available for selection in this column. 

**Dialog Box** The dialog box that will be displayed when the action is clicked on the form, if applicable. For details, see _Dialog Boxes_. 

**Processing Screen** The processing form of Acumatica ERP on which the action will be an option in the **Action** box, in addition to being available on the form for which the action is defined. 

 On a mass-processing form, if you add to a schedule a workflow action that invokes a dialog box in which a user should enter some additional information, then for automated processing, the system uses the default values of this dialog box. 

**Category** The category of the More menu in which the menu command associated with the action will be displayed on the form. 

 This column is not populated if the action has the Navigation: Side Panel type. 


<!-- PAGE_BREAK -->
 Actions | 21 

**Column Description** 

**Status** The status of the action. 

 The status of the action can be one of the following: 

- _Inherited_ : A system action 

- _New_ : An action that you have created 

- _Modified_ : A system action that you have modified 


<!-- PAGE_BREAK -->
 ASPX Editor | 22 

## ASPX Editor 

 Page ID: (SM204590) 

 You use the ASPX Editor page to edit the ASPX code of the particular screen (that is, the form in Acumatica ERP) that you are customizing by using the Screen Editor page. 

 The ASPX Editor page contains the Source Code pane and a toolbar with only the Generate Customization Script button, which is described below. 

 You open the ASPX Editor page by clicking Edit ASPX on the page toolbar of the Screen Editor page of the Customization Project Editor. The name that appears on the page is ASPX Editor: followed by the form ID and then the form name in parentheses. 

### Page Toolbar 

 The page toolbar includes only the following page-specific button. 

 Button Description 

 Generate Customization Script 

 Generates a customization script and saves it to the customization project. You use the Generate Customization Script button instead of a Save button because this action saves to the customization project not the modified ASPX code but the difference between the modified code and the original code of the page. 

### Source Code Pane 

 You use the Source Code pane of the ASPX editor (shown in the following screenshot) instead of the Screen Editor page if you want to use a text editor rather than a visual tool. 

 Figure: The Source Code pane of the ASPX editor 


<!-- PAGE_BREAK -->
 Business Events | 23 

## Business Events 

 Page ID: (AU210010) 

 On this page, you manage the BpEvent items in the customization project. A BpEvent item contains all the data required to recreate the corresponding business event on any instance of Acumatica ERP. 

 You open the Business Events page by clicking Business Events in the navigation pane of the Customization Project Editor. 

### Page Toolbar and More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Command Description 

 Manage Business Events 

 Opens the Business Events (SM302050) form in a new browser tab. 

 Reload from Database 

 Updates the BpEvent items in the customization project if the business events that correspond to these items have been modified on the Business Events (SM302050) form. 

 If you have changed the generic inquiry used in the business event or the import scenario of the business event, you need to update each changed item separately on the corresponding page of the Customization Project Editor. If you have changed the notification template of the business event, the system updates the notification template in the customization project automatically when you update the business event. 

 Table: Add Business Events Dialog Box This dialog box opens when you click Add New Record on the page toolbar. The dialog box contains the following elements. The table toolbar includes only standard buttons. For the list of standard buttons, see Table Toolbar. 

 Element Description 

 Included An unlabeled check box that you select to add the business event in this row to the customization project. 

 Event ID The internal name of the business event. 


<!-- PAGE_BREAK -->
 Business Events | 24 

 Element Description 

 Type The type of the business event, which can be one of the following: 

- _Trigger by Record Change_ : The system processes the subscribers specified on     the **Subscribers** tab when the inquiry results or data provided by the data en-     try form have changed in the ways that meet the conditions specified on the     **Trigger Conditions** tab. The option is available if an inquiry form or data entry     form is specified in the **Screen** box. For details on this type of business event, see     _Business Events: Data Change Processing_. 

- _Trigger by Schedule_ : At the times and frequencies specified on the **Schedules**     tab, the system checks the results of the inquiry and processes the subscribers     specified on the **Subscribers** tab if the inquiry results satisfy the conditions     specified on the **Trigger Conditions** tab. The option is available if an inquiry     form is specified in the **Screen** box. For more information about this type of busi-     ness event, see _Business Events: Scheduled Event Processing_. 

- _Trigger by Action_ : The system processes the subscribers specified on the **Sub-**     **scribers** tab when a user clicks the action specified in the **Action Name** box for     this business event. The option is available if an inquiry form or data entry form     is specified in the **Screen** box. For details on this type of business event, see     _Business Events: User-Triggered Processing of Subscribers_. 

 This dialog box has the following buttons. 

 Save Adds the selected business events to the table on the page and closes the dialog box. 

 Cancel Closes the dialog box without making any changes. 

### Table 

 This table contains the list of business events in the customization project and the basic settings of each of them. The columns of the table are described below. 

 Column Description 

 Object Name The name of the business event in the customization project. 

 Description The description of the business event. 

 Last Modified By The name of the user who last modified the business event in the customization project. 

 Last Modified On The date when the business event was last modified in the customization project. 


<!-- PAGE_BREAK -->
 Code | 25 

## Code 

 Page ID: (AU204000) 

 On this page, you manage the Code items in the customization project. You can add the following Code items: 

- _New Graph_ : A new business logic controller that is derived from the PXGraph<> class 

- _New DAC_ : A data access class that is derived from the PXBqlTable class and the IBqlTable interface 

- _Graph Extension_ : A graph extension that is derived from the PXGraphExtension<> class 

- _DAC Extension_ : A DAC extension (which is also referred to as a _cache extension_ ) that is derived from the     PXCacheExtension<> class 

- _Code File_ : Custom C# code 

- _Customization Plug-in_ : A class that is derived from the CustomizationPlugin class 

 You open the Code page by clicking Code in the navigation pane of the Customization Project Editor. 

### Page Toolbar and More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Button Description 

 Edit Opens the Code Editor page for the Code item selected in the table. You click the row with the item and then click this button. (You can also open the Code Editor page by clicking the link in the Object Name column.) 

 Table: Create Code File Dialog Box This dialog box opens when you click Add New Record on the page toolbar. 

 Element Description 

 The dialog box has the following elements. 

 File Template The type of the Code item that will be created. 

 You select one of the following options: 

- _New Graph_ (default): To create a business logic controller 

- _New DAC_ : To create a data access class 

- _Graph Extension_ : To create a graph extension 

- _DAC Extension_ : To create a DAC extension 

- _Code File_ : To create custom C# code 

- _Customization Plug-In_ : To create a class 


<!-- PAGE_BREAK -->
 Code | 26 

 Element Description 

 Class Name The name of the entity, which is one of the following, depending on the option selected in the File Template box: 

- If _New Graph_ is selected in the **File Template** box, the class name of the business     logic controller 

- If _New DAC_ item is selected in the **File Template** box, the class name that corre-     sponds to the name of the table created in the database 

- If _Code File_ is selected in the **File Template** box, the name of the new class 

- If _Customization Plug-in_ is selected in the **File Template** box, the name of the     plug-in 

 Base Graph The class name of the business logic controller. 

 This box is available only if Graph Extension is selected in the File Template box. 

 Base DAC The DAC on which the DAC extension is based. 

 This box is available only if DAC Extension is selected in the File Template box. 

 Generate Members from Database 

 A check box that you select to indicate that a data access class will be generated with members that correspond to the table columns. 

 This check box is available only if New DAC is selected in the File Template box. 

 This dialog box has the following buttons. 

 OK Adds the Code item to the table on the page and closes the dialog box. 

 Cancel Closes the dialog box without any changes. 

### Table 

 This table lists the Code items in the customization project. The table contains the following columns. 

 Column Description 

 Object Name The name of the Code item in the customization project. 

 Description The description of the Code item. 

 Last Modified By The name of the user who last modified the Code item in the customization project. 

 Last Modified On The date when the Code item was last modified in the customization project. 


<!-- PAGE_BREAK -->
 Code Editor | 27 

## Code Editor 

 Page ID: (AU204000) 

 On this page, you can develop, view, and edit the customization code that has been added to the project. The name that appears on the page is Code Editor: followed by the object name of the Code item whose code you are viewing. 

 You open the Code Editor for any Code item by clicking the link in the table on the Code page or by clicking its name under Code in the navigation pane. You can also open the Code Editor from an Acumatica ERP form by clicking Customization > Inspect Element to open the Element Properties dialog box, and then clicking Actions > Customize Business Logic. 

### Page Toolbar 

 The page toolbar includes standard and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands are listed in the following table. 

 Button Description 

 Move to Ext. Library 

 Launches the operation that converts the current Code item into a file of customization code, adds the file to the extension library project in Microsoft Visual Studio, and removes the item from the customization project. See the To Move a Code Item to the Extension Library for details. 

 The customization project must be bound to an existing extension library project in Visual Studio before you click the Move to Ext. Library button. See Customization Project Editor for details. 

 New Action Opens the Create Action dialog box, which you can use to create a code template for a new action. 

 Open Screen Opens the form bound to the business logic controller if you are editing the customization code of the business logic executed for a form. 

 Override Method Opens the Select Methods to Override dialog box, which you can use to select multiple virtual methods of the business logic controller (BLC) to override. 

 View Source Opens the Source Code Browser (see Source Code ) with the original source code of the BLC if you are editing the customization code of the business logic executed for a form. 

 Table: Create Action Dialog Box This dialog box opens when you click New Action on the page toolbar. By using the dialog box, you can create an action in the business logic controller whose extension you are viewing in the Code Editor. The dialog box contains the following elements. 

 Element Description 

 Action Name The name of the action delegate method. 

 Display Name The name of the action that will be displayed on the applicable Acumatica ERP form. 

 This dialog box has the following buttons. 


<!-- PAGE_BREAK -->
 Code Editor | 28 

 Element Description 

 OK Adds the template of the action declaration to the graph extension and closes the dialog box. 

 Cancel Closes the dialog box without any changes. 

 Table: Select Methods to Override Dialog Box This dialog box opens when you click Override Method on the page toolbar. The dialog box contains the list of the virtual methods of the current BLC and its parent classes. When you override a virtual method, the system generates an overridden method template that includes the delegate declaration of the base method, the PXOverride attribute, and the method declaration that invokes the base method delegate. 

 Column Description 

 The table in the dialog box contains the following columns. 

 Selected A check box that you select to indicate that the virtual method will be overridden in the BLC extension. 

 Type The identifier of the class type that contains the declaration of the virtual method. 

 Method The signature of the virtual method. 

 This dialog box has the following buttons. 

 Save Adds to the graph extension a template of an overridden method for each method selected in the table. 

 Cancel Closes the dialog box without any changes. 

### Source Code Pane 

 You use the Source Code pane of the Code Editor page to view and edit the code for the Code item that you opened from the navigation pane or the Code page. 


<!-- PAGE_BREAK -->
 Conditions | 29 

## Conditions 

 Page ID: (AU201000) 

 You use the Conditions page to construct a condition that can later be specified as a property value for the following items on a particular screen (that is, a form in Acumatica ERP): 

- A UI control 

- An action, including an auto-run action 

- Transition 

 You open the Conditions page by clicking Conditions under the screen ID (of the form for which you are constructing the condition) in the navigation pane of the Customization Project Editor. In the name that appears on the page, Conditions: is followed by the form ID and then the form name in parentheses. 

### Page Toolbar 

 The page toolbar includes only standard buttons. For the list of standard buttons, see Table Toolbar. 

### Condition Properties Dialog Box 

 This dialog box opens when you click Add New Record on the page toolbar of the Conditions page, or when you click a link of an existing condition in the Condition Name column of the table on the page. 

 This dialog box shows the rows that make up the condition. You can add new rows and modify existing rows of the conditions that you have created previously. 

 Table: Condition Properties Dialog Box: Summary Area 

 Element Description 

 Condition Name The name of the condition. 

 Append System Condition 

 A check box that indicates (if selected) that a predefined condition will be used along with the condition specified in the table. 

 System Condition The predefined condition that will be used along with the condition specified in the table. 

 This box is available only if you select the Append System Condition check box. 

 Operator The logical operator to join the system condition specified in the System Condition box and the condition specified in the table in a logical expression. Possible values are And or Or. 

 This box is available only if you select the Append System Condition check box. 

 Table: Condition Properties Dialog Box: Table The table toolbar includes only standard buttons. For the list of standard buttons, see Table Toolbar. 

 Column Description 

 Active A check box that indicates (if selected) that the row is an active condition. 


<!-- PAGE_BREAK -->
 Conditions | 30 

**Column Description** 

**Brackets** The opening bracket or brackets for composing a logical expression with multiple conditions. 

**Field Name** The field to whose value the condition should be applied. 

**Condition** The logical condition that will be applied to the value of the field specified in the^ **Field Name** box and the values in the **Value** and **Value 2** fields, if applicable. 

 One of the following logical conditions should be selected: 

- _Equals_ : Returns _TRUE_ if the field value is equal to the value specified as **Value**. 

- _Does Not Equal_ : Returns _TRUE_ if the field value is not equal to the **Value** value. 

- _Is Greater Than_ : Returns _TRUE_ if the field value is greater than the **Value** value. 

- _Is Greater Than or Equal To_ : Returns _TRUE_ if the field value is greater than or equal to     the **Value** value. 

- _Is Less Than_ : Returns _TRUE_ if the field value is less than the **Value** value. 

- _Is Less Than or Equal To_ : Returns _TRUE_ if the field value is less than or equal to the **Value**     value. 

- _Is Between_ : Returns _TRUE_ if the field value is between the **Value** and **Value 2** values.     (For this option, you must specify both **Value** and **Value 2** .) 

- _Contains_ : Returns _TRUE_ if the field value (string) contains the **Value** value. 

- _Does Not Contain_ : Returns _TRUE_ if the field value (string) does not contain the **Value**     value. 

- _Starts With_ : Returns _TRUE_ if the field value begins with the **Value** value. 

- _Ends With_ : Returns _TRUE_ if the field value ends with the **Value** value. 

- _Is Empty_ : Returns _TRUE_ if the field value is empty (null). 

- _Is Not Empty_ : Returns _TRUE_ if the field value is not empty (not null). 

**From Schema** A check box that indicates (if selected) that in the **Value** and **Value 2** columns, you can select one of the predefined values of the field selected in the **Field Name** column (for example, a document type or a document status). 

**Value** The value to be used in the selected condition. You can select a field, or you can click the Edit button to open the Formula Editor dialog box and create a formula. 

 For the date-related data fields, you can use the date-relative parameters either by selecting the parameter in the Calendar dialog box (if the field is based on a schema field and the From Schema check box is selected) or by using the date-relative parameter in a formula (if the field is not based on a schema field and you use the formula editor). The following date-relative parameters are available: 

- _@Today_ : The business day. 

- _@WeekStart_ and _@WeekEnd_ : The start and end of the current week. The start and end     of the week are determined based on the default system locale or the locale the user     has selected when signing in to Acumatica ERP. System locales are defined on the _Sys-_     _tem Locales_ (SM200550) form. 

- _@MonthStart_ and _@MonthEnd_ : The start and end of the current month. 

- _@QuarterStart_ and _@QuarterEnd_ : The start and end of the current quarter. 

- _@PeriodStart_ and _@PeriodEnd_ : The start and end of the current financial period. The fi-     nancial periods are defined on the _Financial Year_ (GL101000) form. 


<!-- PAGE_BREAK -->
 Conditions | 31 

 Column Description 

 For more information about financial periods in Acumatica ERP, see Managing Financial Periods. 

- _@YearStart_ and _@YearEnd_ : The start and end of the current calendar year. 

 All the date-relative parameters use the date (in UTC) of the server used to run the Acumatica ERP instance as the current date. 

 Additionally, you can modify the date-relative parameters by adding or subtracting integers. The unit of measure of the parameter is determined automatically and the reference point is moved according to the measurement of the parameter—for example, @WeekStart+1 relate to the start of the next week. 

 You can use the following company-related parameters to filter records or show values that depend on a branch or a company selected by a user in the Company and Branch Selection menu: 

- _@branch_ : The branch specified for an entity 

- _@company_ : The company specified for an entity You can also use the following user-relative parameters for the workgroup-related data fields with the _Is In_ or _Is Not In_ condition: 

- @MyGroups: The workgroups in which the current user is a member, excluding the     workgroups that are the subordinates of these workgroups 

- MyWorktree: The workgroups in which the current user is a member, including the     groups that are subordinates of these groups according to the tenant tree structure 

 Value 2 The second value to be used, if the selected condition requires another value. You select a field, or you click the Edit button to open the Formula Editor dialog box and create a formula. 

 For the date-related data fields that are not based on a schema field (that is, the From Schema check box is cleared), you can use one of the date-relative parameters, as described in the previous description. 

 Brackets The closing bracket or brackets for composing a logical expression with multiple conditions 

 . 

 Operator The logical operator to join conditions in a logical expression, which can be And or Or. 

**_Table: Condition Properties Dialog Box: Buttons_** 

The dialog box includes the following buttons. 

 Button Description 

 OK Adds the condition to the list of conditions on the page or updates the existing condition; closes the dialog box. 

 Cancel Closes the dialog box without making any changes. 


<!-- PAGE_BREAK -->
 Conditions | 32 

### Table 

 The table on the page displays the conditions added in the predefined workflow and the conditions that have been added in previous versions of Acumatica ERP. 

 Table: Table Columns 

 Column Description 

 Condition Name The internal name of the condition. When you click the name of the user-defined condition, the Condition Properties dialog box is opened, which shows the properties. 

 Expression The short version of the condition that you have constructed in the table of the Condition Properties dialog box. 

 Status The status of the condition, which can be one of the following: System Read-Only , Inherited , or New. 

 Table: Shortcut Menu If you right-click within the rows of a table, the system opens a shortcut menu. The commands you see in the menu are duplicates of actions on the table toolbar and are listed below. 

 Command Description 

 Refresh Refreshes the data in the table. 

 Delete Deletes the selected row. 


<!-- PAGE_BREAK -->
 Connected Applications | 33 

## Connected Applications 

 Page ID: (AU210030) 

 On this page, you can manage the connected applications in the customization project. Connected applications are client applications that implement OAuth 2.0 or OpenID Connect (OIDC) authorization mechanisms. For details about implementation of OAuth 2.0 or OIDC client applications, see Authorizing Client Applications to Work with Acumatica ERP. 

 You open the Connected Applications page by clicking Connected Applications in the navigation pane of the Customization Project Editor. 

### Page Toolbar and More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Command Description 

 Manage Connected Application 

 Opens the Connected Applications (SM303010) form in a new browser tab. 

 Reload from Database 

 Updates the connected application properties in the customization project if these properties have been modified on the Connected Applications (SM303010) form. 

 Table: Add Connected Application Dialog Box This dialog box opens when you click Add New Record on the page toolbar. 

 Element Description 

 The dialog box contains the following columns. 

 Included A check box that indicates (if selected) that the client application will be added to the customization project. 

 Client Name The name of the client application. 

 Flow The authorization flow that is used by the client application for authentication in Acumatica ERP. 

 This dialog box has the following buttons. 

 Save Adds the selected connected application to the table on the page and closes the dialog box. 

 Cancel Closes the dialog box without any changes. 


<!-- PAGE_BREAK -->
 Connected Applications | 34 

### Table 

 This table lists the connected applications included in the customization project. The table contains the following columns. 

 Column Description 

 Object Name The name of the connected application in the customization project. 

 Description The description of the connected application. 

 Last Modified By The name of the user who last modified the connected application in the customization project. 

 Last Modified On The date when the connected application was last modified in the customization project. 


<!-- PAGE_BREAK -->
 Custom Files | 35 

## Custom Files 

 Page ID: (AU204500) 

 On this page, you manage the File items in the customization project. A File item contains the path to the custom file and the GUID of the file content in the file storage of the database. The path is relative to the website folder. 

 You open the Files page by clicking Files in the navigation pane of the Customization Project Editor. 

### Page Toolbar and More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Command Description 

 Detect Modified Files 

 Runs the check for modified files and opens the Modified Files Detected dialog box if any files have been modified. 

 This process compares each file in the project (in the database) with the original file and detects the files modified in the file system. If any files have been modified, it opens the Modified Files Detected dialog box. 

 Table: Modified Files Detected Dialog Box This dialog box is displayed when you click Detect Modified Files on the More menu if you have modified any files of the customization project in the file system. The dialog box lists all custom and customized files in the website folder. The dialog box contains the following elements. 

 Element Description 

 Selected A check box that you select to update the current file in the customization project. 

 Conflict A check box that indicates (if selected) that the file version in the file system differs from the file version in the customization project. 

 Path The path to the modified file. 

 This dialog box has the following buttons. 

 Update Customization Project 

 Updates the customization project with the file version from the file system. 

 Discard All Changes Keeps the file version that exists in the customization project and discards the changes in the file system. 

 Table: Add Files Dialog Box This dialog box opens when you click Add New Record on the page toolbar. The dialog box contains a table that lists the files that you can add to the customization project. The table toolbar includes only standard buttons. For the list of standard buttons, see Table Toolbar. 


<!-- PAGE_BREAK -->
 Custom Files | 36 

 Element Description 

 The table in this dialog box contains the following columns. 

 Selected A check box that indicates (if selected) that the current file will be added to the customization project. 

 Path The path to the file. 

 Modified The date when the file was modified. 

 Size The size of the file. 

 This dialog box has the following buttons. 

 Save Adds the selected files to the table on the page and closes the dialog box. 

 Cancel Closes the dialog box without adding any files to the page. 

 Table: Edit File Dialog Box This dialog box opens when you click the name of the file in the table on the page. The dialog box contains the following elements. In the dialog box, you can review and edit a text file, or review the content of a binary DLL file. If you have modified a custom file and saved the changes in the database, the changes are not saved in the original file in the file system. If you then click Detect Modified Files on the More menu, the system does not detect a conflict because the file in the database is newer. The system automatically updates the original file in the file system during the publication of the customization project. 

 The dialog box contains the following elements. 

 Element Description 

 Work Area The area where you review and edit the file. 

 This dialog box has the following buttons. 

 Save Saves the changes you have made to the file and closes the dialog box. 

 You cannot save changes to DLL files. 

 Cancel Closes the dialog box without any changes. 

### Table 

 This table contains the list of custom files and the basic settings of each of them. The columns of the table are described below. 

 Element Description 

 Object Name The name of the custom file in the customization project. 

 Third-Party Assembly A check box that indicates (if selected) that the current file is a third-party assembly. 


<!-- PAGE_BREAK -->
 Custom Files | 37 

**Element Description** 

**Description** The description of the custom file. 

**Last Modified By** The name of the user who last modified the file in the customization project. 

**Last Modified On** The date when the file was last modified in the customization project. 


<!-- PAGE_BREAK -->
 Custom Files (Modern UI) | 38 

## Custom Files (Modern UI) 

 Page ID: (AU204600) 

 On this page, you manage the custom files related to the Modern UI of any number of forms in the customization project. A custom file contains code for the customization of the Modern UI of a form. 

 You open the Modern UI Files page by clicking Modern UI Files in the navigation pane of the Customization Project Editor. 

### Page Toolbar and More Menu 

 The page toolbar includes only standard buttons. For the list of standard buttons, see Page Toolbar. 

 Table: Add Files Dialog Box This dialog box opens when you click Add New Record on the page toolbar. The dialog box contains a table that lists the files that you can add to the customization project. The table toolbar includes only standard buttons. For the list of standard buttons, see Table Toolbar. 

 Element Description 

 The table in this dialog box contains the following columns. 

 Selected A check box that indicates (if selected) that this file will be added to the customization project. 

 Path The path to the file. 

 Modified The date when the file was modified. 

 Size The size of the file. 

 This dialog box has the following buttons. 

 Save Adds the selected files to the table on the page and closes the dialog box. 

 Cancel Closes the dialog box without adding any files to the page. 

 Table: Edit File Dialog Box This dialog box opens when you click the name of a file in the table on the page. The dialog box contains the following elements. In the dialog box, you can view and edit the file. The dialog box contains the following elements. 

 Element Description 

 Work Area The area where you view and edit the file. 

 This dialog box has the following buttons. 

 Save Saves the changes you have made to the file and closes the dialog box. 

 Cancel Closes the dialog box without saving any changes. 


<!-- PAGE_BREAK -->
 Custom Files (Modern UI) | 39 

### Table 

 This table contains the list of custom Modern UI files and the basic settings of each of them. The columns of the table are described below. 

 Element Description 

 Object Name The name of the custom file in the customization project. 

 Screen ID The ID of the form the custom file belongs to. 

 Description The description of the custom file. 

 Last Modified By The name of the user who last modified the file in the customization project. 

 Last Modified On The date when the file was last modified in the customization project. 


<!-- PAGE_BREAK -->
 Customization Menu | 40 

## Customization Menu 

 You can access the Customization menu on the form title bar of an opened Acumatica ERP form if your user account is assigned the Customizer role. (For details, see To Assign the Customizer Role to a User Account .) 

 You click Customization on the form title bar to access the customization-related menu commands associated with the form, as shown in the following screenshot. 

 Figure: Customization menu commands 

### Menu Commands 

 You can use the following customization-related menu commands. 

 Command Description 

 Select Project Opens the Select Customization Project dialog box, which you use to select an existing customization project or to specify the name of a new project for all modifications that you are going to perform. 

 Inspect Element Launches the Element Inspector , so that you can select a UI control on the current form and open the Element Properties dialog box for the selected control. You use this dialog box to inspect and customize the control. 

 You can use the keyboard shortcut Ctrl+Alt+Click to inspect elements on popup windows and dialog boxes. 

 If you have selected a customization project, all the modifications that you initiate in the inspector will be added to this current project. Otherwise, the Element Inspector opens the Select Customization Project dialog box. 


<!-- PAGE_BREAK -->
 Customization Menu | 41 

 Command Description 

 Manage User-Defined Fields 

 Opens the Edit User-Defined Fields (CS205020) form, where you can select user-defined fields for the current form from the previously defined list of attributes and user-defined fields (for details, see Managing Attributes and User-Defined Fields ). 

 This command appears only on data entry forms and reports. 

 For details on how to add user-defined user fields, see To Add User-Defined Fields to a Form. 

 Edit Project Opens the Customization Project Editor for the currently selected customization project. 

 Manage Customizations 

 Opens the Customization Projects (SM204505) form. 

 Show State Diagram 

 Opens the State Diagram dialog box, which contains the workflow diagram for the selected form and the Customize Workflow button. 

 If you click the Customize Workflow button, the system opens the Select Customization Project dialog box. In this dialog box, you select an existing customization project (or click New and then specify the name of the customization project to be created in the New Project dialog box) and click OK. This opens the Customization Project Editor, so that you can modify the workflow for the current form. For details, see Workflow Creation: General Information and Diagram View: General Information. 

 If you have only one customization project, the system opens the Customization Project Editor for this project after you click Customize Workflow , without displaying the Select Customization Project dialog box. 

 This command is displayed for forms with workflows without composite states. 

**_Table: Select Customization Project Dialog Box_** 

You use the **Select Customization Project** dialog box to select an existing customization project or to create a new customization project. 

You open the dialog box in the following ways: 

- From the **Customization** menu of a form by clicking **Select Project** 

- From the **Customization** menu of a form by clicking **Edit Project** if there is no currently selected     customization project 

- From the **Element Properties** dialog box if you click **Customize** in the dialog box and there is no currently     selected customization project 

 Element Description 

 The dialog box has the following element. 

 Project Name Provides the ability to select an existing customization project. 

 The dialog box has the following buttons. 

 OK Confirms your selection and closes the dialog box. 

 Cancel Cancels the operation and closes the dialog box. 


<!-- PAGE_BREAK -->
 Customization Menu | 42 

 Element Description 

 New Opens the New Project dialog box, where you can create a new project. 

**_Table: New Project Dialog Box_** 

You use the **New Project** dialog box to create a customization project. The dialog box contains the following elements. 

 Element Description 

 The dialog box has the following element. 

 Project Name The name of the customization project you are creating. 

 The customization project name is used as the namespace if you create an extension library from the project. The first character of the name must be a letter or the underscore symbol. 

 The dialog box has the following buttons. 

 OK Creates an empty customization project with the specified name and closes the dialog box. 

 As soon as you click OK , the system creates a customization project in the database. 

 Cancel Closes the dialog box without creating a customization project. 


<!-- PAGE_BREAK -->
 Customization Project Editor | 43 

## Customization Project Editor 

 Form ID: SM204510 

 You can use the Customization Project Editor to develop and manage the content of a customization project. The editor contains separate pages to add and manage items of the following types in the currently selected customization project. (See Managing Items in a Project for instructions.) 

- Screen (form) 

- Data access class 

- Code (C#) 

- File 

- Generic inquiry 

- Acumatica Report Designer report 

- Site map 

- Database script (custom column or script) 

- Translation (language locale) 

- Integration scenario 

- Shared reusable filter 

- Access rights of roles to forms 

- Wiki changes 

- Analytical report 

- Push notification 

- Mobile app screen You can launch the Customization Project Editor and view its pages only if you have selected a customization project and your user account is assigned the _Customizer_ role. 

 You can launch the editor from any Acumatica ERP form by using the Customization Menu or from the Customization Projects (SM204505) form. 

### Pages of the Customization Project Editor 

 The Customization Project Editor is a set of pages with a common interface, and the interface consists of the following parts: 

- The main menu for working with the customization project (see Item 1 in the following screenshot) 

- The navigation pane, which displays the list of pages used to manage the corresponding project items (Item     2) 

- The main area, which displays the selected page (Item 3, which shows the _Custom Files_ page) 


<!-- PAGE_BREAK -->
 Customization Project Editor | 44 

 Figure: The Customization Project Editor 

 In the navigation pane, a node with a capitalized name can be expanded to give you direct access to items of the appropriate type. 

### Main Menu of the Project Editor 

 The main menu contains the following items and commands. 

 Command Description 

 The File menu contains the following commands. 

 Manage Customization Projects 

 Opens the Customization Projects (SM204505) form in a new window. 

 Edit Project XML Opens the Project XML Editor, which you can use to edit the XML source code of the current customization project, save it to the database, download the project package, and upload a deployment package to replace the project content. 

 Edit Project Items Opens the Edit Project Items page, which you can use to edit the XML source code of a project item. 

 Export Project Package 

 Exports the deployment package of the project—that is, the ZIP file that contains the project. The file has the same name as the exported customization project has. 


<!-- PAGE_BREAK -->
 Customization Project Editor | 45 

**Command Description** 

**Replace from Package** 

 Initiates the import of a previously exported deployment package from a ZIP file. This menu command opens the Open Package dialog box with the Choose File button and the Upload button, which you can use to replace the current project content. 

**Validate Project Prefix** 

 Opens the Customization Project Prefix dialog box, in which you can make sure that all project items contain the needed prefix. 

**Export Project Items Workbook** 

 Generates a workbook with the project items in Excel format. The workbook contains a list of solution objects and integration scenarios grouped by the following types: 

- Site map nodes 

- Mobile site map nodes 

- BLСs and BLC extensions 

- DACs and DAC extensions 

- Push notifications 

- Import or export scenarios 

The **Publish** menu contains the following commands. 

**Publish Current Project** 

 Initiates the process of publishing the current customization project. The system launches a publication process that opens the Compilation window, where you can view a log with information about the process. 

**Validate Current Project** 

 Initiates the process of validating the current project. The system launches the validation process and opens the Compilation window, where you can view a log with information about the process. 

 If both the validation and the compilation of the project are successful, the system makes the Publish button available. You can click this button to finalize the publishing and to update the website. 

**Multiple Projects** Opens the _Customization Projects_ form. 

**Publish with Cleanup** 

 Initiates the process of publishing the current customization project, as the Publish Current Project command does, but with the following difference: When the Acumatica Customization Platform publishes a project that contains a database script, the platform executes the script and tries to avoid executing the script at every publication of the project for optimization purposes. Therefore, the platform keeps information about each script that has been executed at least once and has not since been changed in the database, and omits the repeated execution of such scripts. 

 If you run the Publish with Cleanup operation, the platform cleans all the information about previously executed scripts of the customization project and executes this scripts once more while publishing the project. 

The **Extension Library** menu contains the following commands. 


<!-- PAGE_BREAK -->
 Customization Project Editor | 46 

 Command Description 

 Create New Creates a solution for Microsoft Visual Studio in which you can develop an extension library for the customization project. The solution contains the website and extension library projects. This action also downloads the OpenSolution.bat file. The file contains the absolute path to the .sln file in the file system; you can use this file to open the solution in Visual Studio. 

 By default, the system uses the App_Data\Projects folder of the website as the parent folder for the solution project. If the website folder is outside of the C:\Program Files (x86) and C:\Program Files folders, such as C:\AcumaticaSites\MySite, we recommend that you not change it. Otherwise, we recommend that you specify a parent folder outside these folders to avoid an issue with permission to access files. 

 Bind to Existing Opens the Bind to Extension Library dialog box with the Containing Folder box and the OK and Cancel buttons. In this dialog box, you specify the extension library project in the file system to which the customization code will be moved if you click Move to Ext. Library on the page toolbar of the Code Editor page. 

 Open in Visual Studio 

 Downloads the OpenSolution.bat file, which is used to open the existing solution in Visual Studio. 

 Show Active Extensions 

 Starts the verification of extensions for data access classes and business logic controllers, and opens the Validate Extensions pop-up window to display the validation log. In the log, every error is highlighted in red. We recommend that you verify extensions if you have upgraded legacy DAC customization. 

 Analyze Referenced Assemblies 

 Runs the validation of custom files in the customization project and downloads the CSV file with the report. 

 The Source Control menu contains the following commands. 

 Save Project to Folder 

 Saves the customization project as a set of files to a local folder that is used for integration with source control systems. Opens the Saves Project to Folder dialog box (see To Save a Project to a Local Folder for instructions), in which you can select the name and location of the folder inside a repository. 

 Open Project from Folder 

 Opens the Open Project from Folder dialog box. In this dialog box, you specify the repository (in the Containing Folder box) from which the system should load the customization project. 

**_Table: Customization Project Prefix Dialog Box_** 

In this dialog box, you can make sure that the names of the project items contain the needed prefix. 

 Element Description 

 The dialog box contains the following elements. 

 Project Prefix The prefix that the project items should have. 

 Validation Result The area that displays the results of the validation. 


<!-- PAGE_BREAK -->
 Customization Project Editor | 47 

 Element Description 

 The dialog box has the following buttons. 

 Validate Project Items 

 Runs the validation process. This button becomes available when you enter the prefix in the Project Prefix box and click Save. 

 Save Saves the project prefix to the customization project. 

 Save & Close Saves the project prefix and closes the dialog box. 

 Cancel Closes the dialog box without saving your changes. 

**_Table: Save Project to Folder dialog box_** 

In this dialog box, you specify the folder to which the items of the customization project will be saved. 

 Element Description 

 Parent Folder The path to the folder to save the project items. 

 Project Name The name of the folder. 

 The dialog box has the following buttons. 

 OK Closes the dialog box and saves the project items to the specified folder. 

 Cancel Closes the dialog box without saving your changes. 


<!-- PAGE_BREAK -->
 Customization Projects | 48 

## Customization Projects 

 Form ID: (SM204505) 

 You use this form to do any of the following: 

- Add a new customization project, which is a set of changes and additional files that are used to modify the     Acumatica ERP application 

- Open a customization project for editing in the Customization Project Editor 

- Validate a customization project or multiple projects (see _Validation of a Customization Project_ for details) 

- Publish a customization project (or multiple projects) for a tenant or multiple tenants 

- Cancel the publication of customization projects 

- View the XML of the published customization project 

- Export a customization project as the deployment package 

- Import a customization project from an existing deployment package 

- Delete a customization project 

### Form Toolbar 

 The form toolbar includes standard buttons and form-specific buttons and commands. For the list of standard buttons, see Form Toolbar and More Menu. The form-specific commands can be shown as buttons on the form toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Command Description 

 DAC Attributes (Runtime Validation) 

 Determines whether there are any PXAttributeFamilyAttribute violations on a DAC field. This validation is performed at runtime. 

 DAC Field Types (Runtime Validation) 

 Verifies that the data type of each DAC field matches the field states generated at runtime. This validation is performed at runtime. 

 Export For the selected customization project, exports the deployment package of the customization project—that is, the ZIP file with the project. You first click the row with the project and then click this command. The file has the same name as the exported customization project. 

 You click a project and then click this command. 

 Import Initiates the import of a previously exported deployment package from a ZIP file. When you click this button or command, the system opens the Open Package dialog box, which has the Choose File button and the Upload button to execute the operation. 

 Lookup Definitions (Runtime Validation) 

 Verifies that the DAC fields with lookup boxes defined for a segmented key properly handle foreign key segments by means of PXDimensionAttribute. This validation is performed at runtime. 


<!-- PAGE_BREAK -->
 Customization Projects | 49 

 Command Description 

 Publish Initiates the process of publishing the selected customization projects (that is, those for which you have selected the check box in the Included column). When you click this command, the Compilation dialog box opens to display a log of information about the process. 

 If both the project validation and the compilation of the modified website are successful, the system displays the Publish button in the dialog box; you click this button to finalize the publishing and to update the website. 

 Publish to Multiple Tenants 

 Opens the Publish to Multiple Tenants dialog box, which is used to select the tenants to which the selected customization projects are published and to configure the publishing options. (You select the check box in the Included column for all projects to be published before clicking this command.) After publication is complete, the selected tenants share the customization data that is specific to the opened tenant and stored exclusively in the database. 

 See Customization Projects: Publication to a Multitenant Website or Publication of Customization Projects in a Multitenant Site for details. 

 Replace Highlighted Project Content 

 Initiates the import of a previously exported deployment package from a ZIP file to replace the content of the customization project that is currently selected in the table. This command opens the Open Package dialog box, which has the Choose File button and the Upload button. 

 Screens with Custom Workflow 

 Opens the Screens with Custom Workflow dialog box, which lists the forms whose workflow has been modified. 

 Unpublish All Removes the publication of all listed customization projects from the website. This command does not delete the projects themselves. 

 This command is always available, regardless of whether any customization projects have been published. 

 Validate Certification Status 

 Checks the certification status of all customization projects. 

 Validate Highlighted Project 

 Initiates the process of validating the selected customization project. You first click the row with the project and then click this command. 

 The command opens the Validation Results dialog box, which displays a log of information about the process. 

 Validate Multiple Projects 

 Opens the Choose Projects dialog box, which is used to select the customization projects for validation. 

 View Published XML 

 Displays the Published Customization page, which displays the merged content of the customization projects that are currently published. 

 See Published Customization Page for details. 

### Publish to Multiple Tenants Dialog Box 

 By using this dialog box, you can publish customization projects to multiple tenants at once. 


<!-- PAGE_BREAK -->
 Customization Projects | 50 

 Element Description 

 This dialog box includes a table with the following columns. 

 Selected A check box that indicates (if selected) that the system will publish the selected customization projects on the tenant. 

 Tenant Name The tenant name that is used on the site map. 

 ID The tenant identifier, which was generated automatically by the system when the tenant was created. 

 Parent ID The identifier of the parent tenant that was used to create the tenant in the Acumatica ERP Configuration wizard. 

 This dialog box has the following elements below the table. 

 Apply Changes Only to Database (Skip Website Update) 

 A check box that indicates (if selected) that the system applies to the selected tenants only the database changes introduced by the selected customization packages. 

 If you have published all the selected customization projects in the website for a tenant, you do not need to update website files while publishing to the other tenants. You can apply only the database changes. 

 For details, see Customization Projects: Publication to a Multitenant Website. 

 Execute All Database Scripts (Including Previously Executed) 

 A check box that indicates (if selected) that the system cleans all the information about previously executed scripts of the customization project and executes them once more while publishing the selected projects. 

 If you have published all the selected customization projects in the website for a tenant, you do not need to run the executed scripts once again while publishing the projects to the other tenants. The system will run only any scripts that were not executed earlier. 

 For details, see Customization Projects: General Information. 

 This dialog box has the following buttons. 

 OK Closes the dialog box and initiates the process of publishing the selected projects to each tenant selected in the table of the dialog box. As a result, the published customization content is saved in the database for each selected tenant. 

 Cancel Closes the dialog box without any changes. 

### Screens with Custom Workflow Dialog Box 

 In this dialog box, which opens when you click Screens with Custom Workflow on the More menu, you can view the list of forms with modified workflows for all published customization projects, without the need to open the Customization Project Editor and investigate each customized screen. 

 The dialog box lists only the forms whose workflow has been modified by using Workflow UI. 

 The table toolbar includes only standard buttons. For the list of standard buttons, see Table Toolbar. 


<!-- PAGE_BREAK -->
 Customization Projects | 51 

 Element Description 

 The dialog box includes a table with the following columns. 

 Screen ID The ID of the form for which a custom workflow has been created, or whose workflow has been customized. 

 Screen Name The name of the form for which a custom workflow has been created, or whose workflow has been customized. 

 This dialog box has the following button. 

 Close Closes the dialog box. 

### Choose Projects Dialog Box 

 You use this dialog box, which opens when you click Validate Multiple Projects on the More menu, to select customization projects for validation. 

 The table toolbar includes only standard buttons. For the list of standard buttons, see Table Toolbar. 

 Element Description 

 The dialog box includes a table with the following columns. 

 Included An unlabeled check box that you select to include the customization project specified in the row in the validation process. 

 Published A read-only check box that indicates that the customization project has been published. 

 Project Name The name of the customization project. 

 Description The description of the customization project. 

 This dialog box has the following button. 

 Validate Starts the validation of the selected customization project or projects. 

 Validate and Show All Messages 

 Starts the validation of the selected customization project or projects and displays the results of the validation in the Validation Results dialog box. 

 Cancel Closes the dialog box without running the validation. 

### Validation Results Dialog Box 

 The system displays this dialog box when you click a row with a customization project and then click Validate Highlighted Project on the More menu. The system also displays the dialog box when you click Validate and Show All Messages in the Choose Projects dialog box, 

 The dialog box contains a text area for viewing the results of validation for each customization project selected in the Choose Projects dialog box. The dialog box also contains the OK button, which you click to close it. 


<!-- PAGE_BREAK -->
 Customization Projects | 52 

### Table 

 This table lists all the customization projects that have been created for the instance of Acumatica ERP. The columns of the table are described below. 

 Column Description 

 Included An unlabeled check box that indicates (if selected) that the system will execute the selected command for the project in this row. 

 Published A check box that indicates (if selected) that the project is published. 

 Project Name The unique name of the project. The project name is also a link you can click to open the project in the Customization Project Editor, which is used to configure the project changeset for the website. 

 Level A number representing the level that is used to resolve any conflicts that arise if multiple modifications of the same items of the website are merged. 

 If you leave this box empty, the default value is 0. 

 Use higher values for projects that contain more important changes. 

 Screen Names A system-generated list of the identifiers of the screens that have been modified in the project. 

 Description The description of the customization project, which may be a short explanation of the changes. 

 Certification Status 

 The certification status of each uploaded customization project. A customization project can have one of the following statuses: 

- _Certified_ : The project has been imported into the Acumatica ERP instance and is avail-     able in the database with the certified customization projects. 

- _Not Certified_ : The project has been imported into the Acumatica ERP instance and is     not available in the database with the certified customization projects. 

- _Not Verified_ : The project has been manually modified or created in the current     Acumatica ERP instance. 

- _Not Certified for Current Version_ : The project has been imported into the Acumati-     ca ERP instance and is available in the database with the certified customization     projects, but the major version it has been certified for is not the same as the major     version of the current Acumatica ERP instance. 

 Initials The project prefixes assigned to the customization project provided by Acumatica or ISV partners. 

 Created By The name of the user who created the project. 

 Last Modified On The date when the project was modified most recently. 


<!-- PAGE_BREAK -->
 Customization Projects | 53 

### Published Customization Page 

 The Published Customization page of the form shows the merged XML code of the customization projects that are currently published. You open this page by clicking View Published on the More menu. 

 On the Published Customization page, you can do the following: 

- View the code 

- Download the deployment package that contains the code 

- Upload the deployment package as a ZIP file The Published Customization page includes a toolbar and a text area for viewing XML code. The text area displays the XML content of a merged customization project. This area is not used for editing the XML code. 

 The toolbar buttons are listed below. 

 Button Description 

 Save to Database Is not used in the current version. 

 Download Package Downloads the Customization.zip file, which has the full content of the merged customization project. You can use this file as a joint deployment package to work with the customization project or to publish the final customization on the target website. 

 Upload Package Initiates the upload of a deployment package to Acumatica ERP and makes XML code available in the text area for viewing. 

 Choose File Opens the Open dialog box, in which you select the deployment package file to be uploaded. 


<!-- PAGE_BREAK -->
 Customized Data Classes | 54 

## Customized Data Classes 

 Page ID: (AU203001) 

 On the Customized Data Classes page, you manage the DAC items in the customization project. A DAC item contains data in XML format used by the platform to create an appropriate extension for the original data access class (DAC). 

 You open the Customized Data Classes page by clicking Data Access in the navigation pane of the Customization Project Editor. 

 You cannot create a custom data access class on this page. Instead, you have to use the Code page of the editor. Custom DACs are added to the project as Code items. See To Create a Custom Data Access Class for details. 

### Page Toolbar 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Button Description 

 Add New Record Opens the Select Existing Data Access Class dialog box, in which you select the data class and then click OK. 

 Convert to Extension 

 Converts the class changes into the class extension code used to complete the extension development in either the Code Editor or Microsoft Visual Studio. 

 Edit Opens the Data Class page for the DAC you have selected in the table (by clicking it before clicking this button). 

 Upgrade All Launches the upgrade wizard, which processes all the project items of the DAC and Code types to discover and update the following cases of DAC customization based on the Microsoft Intermediate Language (MSIL) injection technology: 

- A field of a data access class does not contain the StorageName attribute, which     specifies the storage type of the field. 

 In the Acumatica Customization Platform, you must select the way a custom field will be stored in the database when you add the field to a data access class. 

- The code contains a direct reference to a custom field of a row. 

- The code contains a direct reference to an abstract class of a DAC field. 

### Table 

 This table contains the list of customized data classes and the basic settings of each of them. When you click the link in the Name column, the Data Class Editor page for the class is opened. The table contains the following columns. 


<!-- PAGE_BREAK -->
 Customized Data Classes | 55 

**Column Description** 

**Name** The name of the customized data class. 

**Class Name** The full class name. 

**DB Table** The name of the database table that contains the class. 


<!-- PAGE_BREAK -->
 Customized Screens | 56 

## Customized Screens 

 Page ID: (AU201000) 

 You use the Customized Screens page to manage the screens (that is, Acumatica ERP forms) in the customization project. You can add existing screens to the customization project or create new ones. 

 You open the Customized Screens page by clicking Screens in the navigation pane of the Customization Project Editor. 

### Page Toolbar and More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Command Description 

 Create Screen Opens the Create Screen dialog box, in which you specify the settings of the new screen. 

 Customize Existing Screen 

 Opens the Customize Existing Screen dialog box. In this dialog box, you select the screen you want to customize, and click OK. 

 Edit Opens the Screen Editor page for the screen selected in the table. 

 Table: Create Screen Dialog Box This dialog box opens when you click Create Screen on the page toolbar. The dialog box contains the following elements. 

 Element Description 

 The dialog box contains the following elements. 

 Screen ID The ID to be used for the custom Acumatica ERPform, as well as for the screen in the Customization Project Editor. This ID has the XX.**.**.** format, which consists of the following parts: 

- The two-letter code of the functional area in Acumatica ERP 

- The two-digit code indicating the form type as follows: 

- _10_ : Setup form 

- _20_ : Maintenance form 

- _30_ : Data entry form 

- _40_ : Inquiry form 

- _50_ : Processing form 

- _60_ : Report form 

- The two-digit codes (separated by a period) indicating the form's sequential num-     ber 

 Graph Name The unique name of the new graph. 


<!-- PAGE_BREAK -->
 Customized Screens | 57 

 Element Description 

 Graph Namespace The ID of the existing or new namespace for the new graph. By default, the system specifies the customization project name as the namespace ID. 

 Page Title The title to be used as the form title in Acumatica ERP. 

 Template The ASPX page template to be used for the custom form, which can be one of the following: 

- _Form (FormView)_ : A record-editing page with one PXFormView container 

- _Grid (GridView)_ : A record-editing page with one PXGrid container 

- _Tab (TabView)_ : A record-editing page with one PXTab container 

- _FormTab_ : A record-editing page with PXFormView and PXTab containers 

- _FormGrid (FormDetail)_ : A master-detail editing page with PXFormView and PX-     Grid containers 

- _TabGrid (TabDetail)_ : A master-detail page with PXTab and PXGrid containers 

 This dialog box has the following buttons. 

 Create Adds the new screen with the specified properties to the list of customized screens on the page and closes the dialog box. Also, adds the Delete access rights for the Customizer role to the Access Rights page and specifies the Apply and Keep merge rule for these access rights. 

 Cancel Closes the dialog box without making any changes. 

### Table 

 This table contains the list of customized screens and basic settings of each of them. When you click the link in the Screen ID column, the Screen Editor page is opened for the selected screen. The columns of the table are described below. 

 Column Description 

 Screen ID The ID of the form, which is a link that you click to open the Screen Editor page for the form. 

 Title The name of the form as it is displayed in Acumatica ERP. 

 Is New A check box that indicates (if selected) that the screen has been created by a customizer. 

 This check box is selected automatically for new screens and is read-only. 

 Last Modified By The name of the user who last modified the screen in the Customization project. 

 Last Modified On The date when the screen was last modified in the customization project. 


<!-- PAGE_BREAK -->
 Data Class | 58 

## Data Class 

 Page ID: (AU203001) 

 You use the Data Class page to develop the content of the extension for a data access class (DAC). The full name of the page is Data Class: , followed by the name of the customized DAC. By using this page, you can do the following: 

- Customize the attributes of the existing fields of a DAC 

- Add custom fields to a DAC 

- For a selector field, add, delete, and sort the columns of the associated lookup table 

- Review the modifications made to an original class 

- View the source code of an original data access class 

- Navigate to the form on which a field of a class is used 

 While performing customization, you can open this page in the following ways: 

- From the **Element Properties** dialog box, which you access by clicking **Customization Menu >**     **Inspect Element** , if you click **Actions > Customize Data Fields** 

- From the Customized Data Classes page of the Customization Project Editor, by clicking the     link in the **Name** column of a DAC 

- From the navigation pane of the Customization Project Editor, by clicking an item listed under     **Data Access** 

 The platform gives you advanced possibilities to control the field customization by using additional attributes in the DAC extension. See Customization of Field Attributes in DAC Extensions of Customization Framework for details. 

### Page Toolbar and More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Button Description 

 Change Attributes of Base Field 

 Opens the Change Existing Field dialog box, which you can use to add an existing field of the DAC to the customization project. 

 Create New Field Opens the Create New Field dialog box, which you can use to add a new custom field to the DAC. 

 Edit Attributes Opens the Customize Attributes dialog box, which you can use to customize the attributes of the selected field. Before clicking the command, in the table of the Customized Fields pane, you click the row with the field. This command is unavailable if you are creating a new custom field. 

 This command is unavailable if you click a row with a new field before clicking the button. 


<!-- PAGE_BREAK -->
 Data Class | 59 

 Button Description 

 Edit Selector Columns 

 Opens the Customize Selector Columns dialog box, in which you can modify the columns in the lookup table that corresponds to the selector field you have selected in the Customized Fields pane. 

 This command is available only if you have selected a selector field before clicking Edit Selector Columns on the More menu. 

 Open Screen Opens the primary form of Acumatica ERP for the DAC. 

 If there is a primary business logic controller (BLC) for the class, then the primary form is the form bound to this container. Otherwise, the primary form is the form bound to the BLC in which the class is the main DAC of the primary view. 

 View Source Opens the Data Access tab of the Source Code (SM204570) form, which displays the DAC source code. 

### Create New Field Dialog Box 

 This dialog box opens when you click Create New Field on the More menu. You can also open the dialog box by clicking New Field on the Add Data Fields tab of the Screen Editor page. 

 Element Description 

 The dialog box contains the following elements. 

 Field Name The name of the field in the DAC. Because this is a custom field, the Usr prefix must begin its name. If you do not add the prefix, the system adds it automatically when the box loses focus. 

 Display Name The name of the field to be displayed on the form. The specified string is inserted as the DisplayName parameter of the PXUIField attribute of the field. 

 Storage Type The storage type for the field. 

 The storage type can be one of the following: 

- _NonPersistedField_ : An unbound field of the DAC. The unbound field is added only to the     data access class and is not mapped to the database. 

- _DBTableColumn_ (default): An ordinary bound field. The platform adds the database col-     umn to the base table by altering the base table schema. 

- _NameValuePair_ : A "name-value" bound field. The platform stores the field value in a     dedicated table of the database without altering the schema of the base table. 

 Data Type The data type to be used for a custom field. The type can be one of the following: string , int (default), bool , decimal , datetime , and guid. 

 Length The maximum field length. For the string type, you enter the maximum number of symbols in the field value; for the decimal type, you enter the precision of the value (the maximum total number of decimal digits that will be stored, both to the le of the decimal point and to the right of it). 

 This box appears if you have selected the string or decimal data type. 


<!-- PAGE_BREAK -->
 Data Class | 60 

 Element Description 

 Decimal The scale of the value (that is, the number of decimal digits that will be stored to the right of the decimal point). 

 This box appears if you have selected the decimal data type. 

 This dialog box has the following buttons. 

 OK Adds the new field with the specified properties to the data access class and closes the dialog box. The field appears in the list of customized fields of the class on the page. 

 Cancel Closes the dialog box without making any changes. 

### Change Existing Field Dialog Box 

 This dialog box opens when you click Change Attributes of Base Field on the More menu. You use the dialog box to change the attributes of a field of the current DAC. 

 Element Description 

 The dialog box contains the following box. 

 Field Name The existing field (of the DAC) whose attributes you want to change. 

 This dialog box has the following buttons. 

 OK Adds the selected field to the list of the customized fields of the data access class, and closes the dialog box. You then customize the attributes of this field in the Source Code pane. 

 Cancel Closes the dialog box without adding any fields to the list of customized fields. 

### Customize Selector Columns Dialog Box 

 This dialog box opens when you click Edit Selector Columns on the More menu. In the dialog box, you can add, delete, and sort columns to customize the lookup table that is opened on the form when the user clicks the magnifier button. 

 Table: Customize Selector Columns Dialog Box: Table Toolbar The table toolbar includes standard buttons and buttons that are specific to this table. For the list of standard buttons, see Table Toolbar. The table-specific buttons are listed below. 

 Button Description 

 Add Columns Opens the Add Columns to Selector dialog box, which you use to add columns to the lookup table that corresponds to the selector field. 

 Up Moves up the selected field, so that the column moves le in the lookup table. 

 Down Moves down the selected field, so that the column moves right in the lookup table. 

 Table: Customize Selector Columns Dialog Box: Table Columns The table has the following columns. 


<!-- PAGE_BREAK -->
 Data Class | 61 

 Column Description 

 Column Name The value of the DisplayName parameter of the PXUIField attribute of the field. 

 Data Field The name of the public virtual property of the field in the DAC. 

 Table: Customize Selector Columns Dialog Box: Buttons The dialog box contains the following buttons. 

 Button Description 

 OK Applies the modifications to the lookup table associated with the selector field. 

 As a result, the PXCustomizeSelectorColumns attribute is added to the selector field, and you can view the attribute in the Customize Attributes area of the Data Class page. This attribute defines the new set and order of the columns in the lookup table. 

 Cancel Closes the dialog box without making any changes. 

### Add Columns to Selector Dialog Box 

 This dialog box opens when you click Add Columns in the Customize Selector Columns dialog box. You use the dialog box to add one column to the lookup table that corresponds to the selector field or to add multiple columns to the lookup table at once. 

 Table: Add Columns to Selector Dialog Box: Tabs The tabs in the dialog box display the filtered lists of fields, as described in the following table. 

 Tab Description 

 All Displays all fields. 

 Selector Displays only selector fields. 

 Custom Displays new custom fields. 

 Table: Add Columns to Selector Dialog Box: Table The dialog box contains the following columns. 

 Element Description 

 Selected A check box that you use to select the fields for which columns will be added to the lookup table that corresponds to the selector field. 

 Column Name The value of the DisplayName parameter of the PXUIField attribute of the field. 

 Data Field The name of the public virtual property of the field in the DAC. 

 Table: Add Columns to Selector Dialog Box: Buttons The dialog box contains the following buttons. 


<!-- PAGE_BREAK -->
 Data Class | 62 

 Button Description 

 OK Applies the modifications and adds the selected columns to the table of the Customize Selector Columns dialog box. 

 Cancel Closes the dialog box without making any changes. 

### Customize Attributes Dialog Box 

 This dialog box opens when you click a field on the Data Class page and then click Edit Attributes on the More menu. In the dialog box, you edit the attributes of the selected field. 

 Table: Customize Attributes Dialog Box: Table Toolbar The table toolbar includes standard buttons and buttons that are specific to this table. For the list of standard buttons, see Table Toolbar. The table-specific buttons are listed below. 

 Button Description 

 Delete Deletes the attribute selected in the Attributes column. 

 As a result, the [PXRemoveBaseAttribute(typeof(AttrNameAttribute))] attribute is added to the field, and you can view the attribute in the Customize Attributes area of the Data Class page. 

 Table: Customize Attributes Dialog Box: Table Columns The columns of the table are described below. 

 Element Description 

 Attributes The list of field attributes. 

 Property The name of the parameter of the attribute selected in the Attributes column. 

 Value The original value of the parameter selected in the Attributes column. 

 You can enter any string as the parameter value without the system performing type validation. If the value of the customized parameter has an incorrect type, it causes a validation error during the publication of the customization project. 

 Table: Customize Attributes Dialog Box: Buttons The dialog box contains the following buttons. 

 Button Description 

 OK Applies the modifications to the field. 

 As a result, the [PXCustomizeBaseAttribute(typeof(AttrNameAttribute), "ParameterName", NewValue)] attribute is added to the field for the modified parameter. You can view the source code of the attribute in the Customize Attributes area of the Data Class page. 

 Cancel Closes the dialog box without making any changes. 


<!-- PAGE_BREAK -->
 Data Class | 63 

### Customized Fields Pane 

 The Customized Fields pane (the le pane of the Data Class page) contains a table that lists all of the currently customized fields of the DAC. In the table, you select a field, and then you view or edit its attributes in the Source Code pane (the right pane of this page). The table has a single column: Field Name. 

 The table toolbar includes only standard buttons. For the list of standard buttons, see Table Toolbar. 

### Source Code Pane 

 You use the Source Code pane (the right pane of the page) to customize the attributes of the field that is currently selected in the table of the Customized Fields pane. 

 The title of the pane contains the name and type of the selected field. The type of the field is specified in parentheses and can be one of the following: New Field or Customized Existing Field. 

 The work area contains the following elements. 

 Element Description 

 Customize Attributes The area in which you can edit the source code of the attributes of the selected field. 

 Drop-down list The way in which the system applies the changes to the field attributes. 

 The following options are available: 

- _Keep Original_ : The original attributes remain on the field until you select another     option in this box. 

- _Replace Original_ : The original attributes are replaced on the field with the custom     attributes specified in the **Customize Attributes** area. 

- _Append to Original_ (default): The custom attributes are added to the end of the list     of the original attributes of the data field. If you use this option, make sure that     you do not duplicate attributes on the field. This element is available for only an existing customized field. 

 If you want to change the original attributes in the Customize Attributes area, before typing any text in the area, select the Replace Original option. The original attributes will be copied to the Customize Attributes area. 

 Original Attributes The area in which you view the source code of the original attributes of the selected field. 


<!-- PAGE_BREAK -->
 Database Scripts | 64 

## Database Scripts 

 Page ID: (AU209000) 

 On this page, you can manage the Sql and Table items of the customization project. 

 An Sql item contains a custom database table definition or a custom SQL script that has to be executed while the customization project is published. A Table item contains a description of the custom columns added to a table for bound custom fields created in the appropriate data access class. 

 When you create a custom table in the database, we recommend that you add the table schema to the customization project, as described in To Add a Custom Table to a Project. To create other database objects or insert data into the tables, you have to compose the corresponding SQL script and add the script to the customization project, as described in To Add a Custom SQL Script to a Project. 

 You open the Database Scripts page by clicking Database Scripts in the navigation pane of the Customization Project Editor. 

### Page Toolbar and More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Command Description 

 Add Custom Column to the Table 

 Opens the Add Custom Column to Table dialog box, in which you select a column of an existing table to be added to the customization project. 

 Add Custom Table Schema 

 Opens the Add Custom Table Schema dialog box, in which you select the table to be added to the customization project, and then click OK. 

 Add Script Opens the Edit SQL Script dialog box, which you use to add and edit a custom SQL script. 

 Increase Column Length 

 Opens the Column Length Increase dialog box, in which you can specify the new length for the column. 

 Reload from Database 

 Updates the Table items in the customization project if the business events that correspond to these items have been modified by using a database administration tool, such as SQL Server Management Studio. 

### Add Custom Column to Table Dialog Box 

 This dialog box opens when you click Add Custom Column to Table on the More menu. In the dialog box, you can add custom columns of an existing table of Acumatica ERP to the customization project. 


<!-- PAGE_BREAK -->
 Database Scripts | 65 

 Element Description 

 The dialog box contains the following elements. 

 Table The name of the table to which the column will be added. 

 Field Name The name of the column to be added. 

 Data Type The type of the column to be added. 

 This dialog box has the following buttons. 

 OK Adds the Table item to the customization project and closes the dialog box. 

 Cancel Closes the dialog box without making any changes. 

### Edit SQL Script Dialog Box 

 This dialog box opens when you click Add Script on the page toolbar or More menu. You can also open it by clicking the name of the script in the Object Name column of the table on the page, or by selecting the row with the script and clicking Edit on the page toolbar. The dialog box contains the following elements. 

 Element Description 

 The dialog box contains the following elements. 

 Script Name The name of the SQL script. 

 Priority The priority of the script. The priority can have a value that ranges from 0 to 100. By default, the priority is 0. 

 Unlabeled text area 

 A text area that you can use to view and edit a custom SQL script. 

 This dialog box has the following buttons. 

 Specify Database Engine 

 Opens the Specify Database Engine dialog box. In this dialog box, you select the attribute of the script that indicates on which database servers the script can be executed (Microsoft SQL Server, MySQL Server, or both), and then click OK. 

 The following options are available: 

- _Skip Batch on MySQL Server_ : Adds the --[mysql: Skip] attribute to the end of the     text in the text area of the script editor. 

- _Skip Batch on Microsoft SQL Server_ : Adds the --[mssql: Skip] attribute to the end     of the text in the text area of the script editor. 

- _Use Interpreter_ : Adds the --[VmSql] attribute to the end of the text in the text area of     the script editor. For more information about the database script attributes, see _Using the SQL Script Attrib- utes_. 

 OK Saves the custom SQL script to the customization project and closes the dialog box. 


<!-- PAGE_BREAK -->
 Database Scripts | 66 

 Element Description 

 Cancel Closes the dialog box without making any changes. 

### Column Length Increase Dialog Box 

 This dialog box opens when you click Increase Column Length on the More menu. You use the dialog box to increase the size of a text column of an existing table of Acumatica ERP. 

 Element Description 

 The dialog box contains the following elements. 

 Table The table in which the column should be modified. 

 Field Name The name of the column that should be modified. 

 Only text fields are available in the list because only their length can be changed. 

 Data Type Read-only. The current type and size of the specified column. 

 New Length The new length of the text field. 

 This dialog box has the following buttons. 

 OK Creates a script to alter the column in the application database, adds the script to the table on page, and closes the dialog box. 

 Cancel Closes the dialog box without making any changes. 

### Edit Table Columns Dialog Box 

 This dialog box opens when you click the name of an item of the Custom Columns type in the Object Name column in the table on the page, or when you select the row with the name of the custom column and click Edit on the page toolbar. You use the dialog box to edit the custom table. 

 The dialog box contains the following elements. 

 Table: Edit Table Columns Dialog Box: Table Toolbar The table toolbar includes standard buttons and buttons that are specific to this table. For the list of standard buttons, see Table Toolbar. The table-specific buttons are listed below. 

 Button Description 

 Add Provides the following menu commands: 

- **Add New Column** : Opens the **Add Custom Column to Table** dialog box, in which you     can add custom columns of the selected table. 

- **Column Length Increase** : Opens the **Column Length Increase** dialog box, in which     you can increase the size of a text column of the selected table. 


<!-- PAGE_BREAK -->
 Database Scripts | 67 

 Table: Edit Table Columns Dialog Box: Table Columns The columns of the table are described below. 

 Element Description 

 Field Name The name of the field of the database table. 

 Script Type The type of the database script applied to the table. 

 Data Type The type of the field of the database table. 

 Table: Edit Table Columns Dialog Box: Button The dialog box contains the following button. 

 Button Description 

 Done Saves the custom columns of the table to the customization project and closes the dialog box. 

### Table 

 The table on the page contains the following columns. 

 Column Description 

 Object Name The name of the item added to the customization project. 

 Type The type of the item added to the customization project. 

 This column can contain one of the following options: 

- _Custom Columns_ 

- _Custom Table Schema_ 

- _Script_ 

 Priority The priority of the SQL script. 

 This is the value specified in the Edit SQL Script dialog box. The column can contain a value that ranges from 0 to 100. 


<!-- PAGE_BREAK -->
 Dashboards | 68 

## Dashboards 

 Page ID: (AU206004) 

 On this page, you manage the Dashboard items in the customization project. A Dashboard item contains the dataset of a custom or customized dashboard. 

 You open the Dashboards page by clicking Dashboards in the navigation pane of the Customization Project Editor. 

### Page Toolbar and More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Command Description 

 Manage Dashboards 

 Opens the Dashboards (SM208680) form in a new browser tab. 

 Reload from Database 

 Updates the Dashboard items in the customization project if the dashboards that correspond to these items have been modified on the Dashboards (SM208680) form. 

 Table: Add Dashboards Dialog Box This dialog box opens when you click Add New Record on the page toolbar. The dialog box displays all the custom and customized dashboards that exist in your Acumatica ERP instance. You can select multiple dashboards to add them to the project simultaneously. The dialog box contains the following elements. 

 Element Description 

 The table toolbar includes only standard buttons. For the list of standard buttons, see Table Toolbar. 

 The table the following columns. 

 Included A check box that indicates (if selected) that the current dashboard will be added to the customization project. 

 Name The name of the dashboard. 

 Site Map Location The ID of the dashboard. 

 This dialog box has the following buttons. 


<!-- PAGE_BREAK -->
 Dashboards | 69 

 Element Description 

 Save Adds the selected dashboard to the table on the page and closes the dialog box. 

 The system also adds to the customization project the needed Generic Inquiry , Site Map , and Wiki items for generic inquiries, site map nodes, and wiki pages, respectively, associated with the dashboard. 

 The system automatically includes in the customization project information about the workspace to which the dashboard has been added on the UI, along with other information about the dashboard. 

 Cancel Closes the dialog box without making any changes. 

### Table 

 The table on the page lists the dashboards in the customization project. The columns of the table are described below. 

 Column Description 

 Object Name The name of the dashboard in the customization project. 

 Description The description of the dashboard. 

 Last Modified By The name of the user who last modified the dashboard in the customization project. 

 Last Modified On The date when the dashboard was last modified in the customization project. 


<!-- PAGE_BREAK -->
 Dialog Boxes | 70 

## Dialog Boxes 

 Page ID: (AU201040) 

 On this page, you configure the dialog boxes that are displayed when a user performs particular actions on the form. In a dialog box, the user enters settings and clicks buttons to perform the applicable action and change the state of the entity associated with the form. 

 You open the Dialog Boxes page by clicking Dialog Boxes under the screen ID (of the form for which you are adding or modifying dialog boxes) in the navigation pane of the Customization Project Editor. In the name that appears on the page, Dialog Boxes is preceded by the form ID and then the form name in parentheses. 

### Page Toolbar and More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Command Description 

 Preview Dialog Box Gives you the ability to preview the selected dialog box. 

 View Changes Opens the Changes dialog box, which you use to view the changes in the dialog box. 

 This command is available only if the selected dialog box is inherited—that is, based on a predefined dialog box. 

 Table: Changes Dialog Box You use this dialog box, which opens when you click View Changes , to view the source code of the dialog box; the changes to the currently selected element are highlighted in red. The dialog box also contains the following buttons. 

 Button Description 

 Revert Changes Returns the dialog box to the predefined state. 

 This button is available if you have made changes to the dialog box. 

 Close Closes the dialog box. 

### Dialog Boxes Pane 

 The Dialog Boxes pane (the le pane of the page) contains the list of dialog boxes. In the table, you select a dialog box, and then you view its settings in the Settings pane (the right pane of the page). The table has a single column: Dialog Box Name. 

 The table toolbar includes only standard buttons. For the list of standard buttons, see Table Toolbar. 

 You add a new dialog box by clicking Add Row on the table toolbar. In the dialog box that is opened, you specify the name of the dialog box and click OK. 


<!-- PAGE_BREAK -->
 Dialog Boxes | 71 

### Summary Area 

 The Summary area, located in the right pane, contains the summary settings of the dialog box. 

 Element Description 

 Title The name of the dialog box as it is displayed in Acumatica ERP. 

 Dialog Box Name A read-only box that contains the internal name of the dialog box. 

 Status A read-only box that indicates the status of the dialog box, which can be one of the following: 

- _Inherited_ : A system dialog box 

- _New_ : A dialog box that you have created 

- _Modified_ : A system dialog box that you have modified 

 Number of Columns The number of columns in which fields are arranged in the dialog box. 

 Actions The action or actions that cause the system to display the dialog box. 

### Dialog Box Fields Table 

 The Dialog Box Fields table displays the list of fields corresponding to the dialog box selected in the Dialog Boxes pane. 

 Table: Table Toolbar The table toolbar includes standard buttons and buttons that are specific to this table. For the list of standard buttons, see Table Toolbar. The table-specific buttons are listed below. 

 Button Description 

 Combo Box Values Opens the Combo Box Values dialog box, in which you can configure the values displayed for the field selected in the Dialog Box Fields table. 

 Table: Table Columns This table lists the fields in the dialog box that is selected in the Dialog Boxes pane. The columns are described below. 

 Column Description 

 Active A check box that indicates (if selected) that the element corresponding to the selected field is displayed in the dialog box. 

 Schema Field The database field selected as the schema for the field. 

 In this column, you can also select fields that correspond to the following types of elements: a check box, a combo box, and a box with rich text editor support. 

 Field Name The internal name of the field. 

 Title The name of the element that is displayed in the dialog box. 


<!-- PAGE_BREAK -->
 Dialog Boxes | 72 

 Column Description 

 From Schema A check box that indicates (if selected) that the field value from the database should be used. 

 Default Value The value that is displayed for the field by default. 

 Required An indicator of when the element corresponding to the field is marked as required in the dialog box. 

 By default, the column is empty, indicating that the element is never required. If the column is not empty, it can contain one of the following: 

- _True_ : The element is always marked as required. 

- _False_ : The element is never marked as required. 

- Condition: The condition that causes the element to be required if it is met. If any     conditions are specified on the _Conditions_ page for the applicable screen, they be-     came available for selection in the column. 

 Hidden The condition under which the element corresponding to the field is not displayed in the dialog box. 

 By default, the column is empty, indicating that the field is always visible. If the column is not empty, it can contain one of the following: 

- _True_ : The element is always hidden. 

- Condition: The condition that causes the element to be hidden if it is met. If any     conditions are specified on the _Conditions_ page for the applicable screen, they are     available for selection in this column. 

 Column Span The number of columns spanned by the element corresponding to the field. 

 Control Size The width of the grid column. 

 Status The status of the field, which can be one of the following: 

- _Inherited_ : A system field 

- _New_ : A field that you have added 

- _Modified_ : A system field that you have modified 

**_Table: Combo Box Values Dialog Box_** 

This dialog box opens if you click a field in the **Dialog Box Fields** table and then click **Combo Box Values** on the table toolbar. You can then specify the source of the values of the field you have selected. If the source is explicitly specified values, you can enter the values in this dialog box. 

 Element Description 

 The Summary area of the dialog box contains the following element. 

 Source of Values The source of the values for the field, which can be one of the following options: 

- _Take from Source State_ (default): The values from the source state of the transition are     used. 

- _Take from Target State_ : The values from the target state of the transition are used. 

- _Specify Explicitly_ : The system uses the values specified in the table in this dialog box. If     you select this option, the table with the dialog box values appears in the dialog box. 


<!-- PAGE_BREAK -->
 Dialog Boxes | 73 

**Element Description** 

This table contains the values of the combo box of the selected field, which appears if _Specify Explicitly_ is selected as the source of the value. 

The table toolbar includes only standard buttons. For the list of standard buttons, see _Table Toolbar_. 

The table has the following columns. 

**Active** A check box that indicates (if selected) that the current value is available for the field that was selected in the **Dialog Box Fields** table. 

**Value** The internal name of the field value. 

**Description** The display name that will be shown in the drop-down box for the selected field. 

This dialog box has the following buttons. 

**OK** Closes the dialog box and applies the changes. 

**Cancel** Closes the dialog box without applying any changes to the combo box values of the selected field. 


<!-- PAGE_BREAK -->
 Edit Project Items | 74 

## Edit Project Items 

 You use the Edit Project Items page to edit and review the items of a customization project. 

 You open the page by clicking File > Edit Project Items on the main menu of the Customization Project Editor. 

### Page Toolbar 

 The page toolbar includes standard and page-specific buttons. For the list of standard buttons, see Page Toolbar. The page-specific buttons are listed below. 

 Button Description 

 Get Package Imports the contents of the customization project as a ZIP file. 

### Table 

 This table contains the list of all items added to the customization project and the basic settings of each item. The columns of the table are described below. 

 Column Description 

 Object Name The ID of the item. 

 Type The type of the item. This column can have the following values: 

- _Automation_ 

- _BpEvent_ 

- _Code_ 

- _Dashboard_ 

- _EntityEndpoint_ 

- _File_ 

- _GenericInquiryScreen_ 

- _Locale_ 

- _MobileSiteMap_ 

- _MobileSiteMapWorkspaces_ 

- _OAuthClient_ 

- _Page_ 

- _PushNotification_ 

- _ReportDefinition_ 

- _Report_ 

- _ScreenWithRights_ 

- _SharedFilter_ 

- _SiteMapNode_ 

- _Sql_ 


<!-- PAGE_BREAK -->
 Edit Project Items | 75 

 Column Description 

- _Table_ 

- _Webhook_ 

- _WikiArticle_ 

- _XportScenario_ 

 Description The description of the item. 

 Created By The name of the user who added the item to the customization project. 

 Creation Date The date when the item has been added to the customization project. 

 Last Modified By The name of the user who last modified the item in the customization project. 

 Last Modified On The date when the item was last modified in the customization project. 

### Source Pane 

 You use the Source pane of this page to view and edit the contents of the item selected in the table. 


<!-- PAGE_BREAK -->
 Element Inspector | 76 

## Element Inspector 

 For any visual element on a form, you can use the Element Inspector to do the following: 

- View information about the element, such as its control type, data access class, data field, data view,     business logic controller, actions (if applicable), and drop-down control values 

- View the ASPX source code with the UI control for the inspected element 

- View the HTML source code with the layout definition of the UI control for the inspected element 

- View the TypeScript source code with the presentation logic of the UI control for the inspected element 

- View the source code of the data access class that provides data for the inspected element 

- View the source code of the business logic executed for the inspected element 

- Start the customization of the inspected element 

 While you are viewing a form, you can activate the Element Inspector from the Customization Menu. If you need to activate the Element Inspector for a pop-up panel, dialog box, or other UI element for which the Customization menu is unavailable, you can press Control+Alt. 

 Aer the Element Inspector is activated, the cursor indicates that you can select a UI element to inspect it. If you click an element, the Element Inspector opens the Element Properties Dialog Box for the element. 

### Element Properties Dialog Box 

 The Element Inspector opens the Element Properties dialog box when you have selected a UI element to inspect. The dialog box contains the following elements. 

 Element Description 

 Control Type The type of the inspected UI element. 

 Data Class The name of the DAC to which the field for the inspected element belongs. 

 Data Field The string value of the DataField property of the inspected UI element. (It corresponds to the name of the field in the DAC.) 

 View Name The name of the data view that provides data for the inspected UI element. 

 Business Logic The name of the BLC bound to the form. 

 Description The description of the inspected UI element. When you click More , the system opens a pane that partially overlaps the working area of the screen and contains the complete element's description. 

 Action Name The name of the action of the inspected toolbar button or menu command. 

 The dialog box has the following buttons. 

 Drop-Down Values Opens the Drop-Down Values dialog box, which lists all possible values of the control and the corresponding values that are saved to the database. 

 The button is displayed only if you have selected a drop-down control. 


<!-- PAGE_BREAK -->
 Element Inspector | 77 

 Element Description 

 Customize Launches the Customization Project Editor, which opens on the Screen Editor page for the form that contains the inspected element. 

 Actions Opens the Actions menu with the following commands: 

- **Customize Business Logic** : Creates a graph extension template for the BLC that is     bound to the form, adds the template code to the customization project, and opens     the Customization Project Editor on the _Code Editor_ page, which loads the BLC exten-     sion template so that you can edit it. 

- **Customize Data Fields** :     Opens the Customization Project Editor on the _Data Class_ page so that you can cus-     tomize the inspected element attributes in the **Edit Attributes** area. 

- **View ASPX Source** : Opens the **Screen ASPX** tab of the _Source Code_ browser with the     ASPX source code of the current form. 

- **View HTML Source** : Opens the **Screen HTML** tab of the _Source Code_ browser with     the HTML source code of the current form. 

- **View TypeScript Source** : Opens the **Screen TypeScript** tab of the _Source Code_     browser with the TypeScript source code of the current form. 

- **View Business Logic Source** : Opens the **Business Logic** tab of the _Source Code_     browser with the source code of the BLC that is bound to the form. 

- **View Data Class Source** : Opens the **Data Access** tab of the _Source Code_ browser     with the source code of the DAC to which the field for the inspected element belongs. 

 Cancel Cancels the inspection of the element and closes the dialog box. 

 If you open the Customization Project Editor or the Source Code browser, you can access any source code of the website—not only the source code of the inspected element and the current form, DAC, and BLC. 

### Drop-Down Values Dialog Box 

 In the dialog box, you can view all possible values of the selected drop-down control and the corresponding values that are saved to the database. For details on the internal names of drop-down control values, see Configuration of Drop-Down Lists. 

 You open this dialog box by clicking Drop-Down Values in the Element Properties dialog box. The dialog box contains the following elements. 

 Element Description 

 Value The internal value of the drop-down control that is saved to the database. 

 Description The display name that will be shown in the drop-down box for the selected field. 

 The dialog box has the following button. 

 Close Closes the dialog box. 


<!-- PAGE_BREAK -->
 Event Handlers | 78 

## Event Handlers 

 Page ID: (AU201070) 

 You use this page to create and modify event handlers for a particular screen (that is, a form in Acumatica ERP). 

 The page automatically displays the event handlers added in the predefined workflow. 

 You open the Event Handlers page by clicking Event Handlers under the screen ID (of the form for which you are adding or modifying event handlers) in the navigation pane of the Customization Project Editor. In the name that appears on the page, Event Handlers is preceded by the form ID and then the form name in parentheses. 

### Page Toolbar and More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Command Description 

 Reverse Changes Returns the selected event handler to its predefined state. 

 View Changes Opens the Changes dialog box, in which you can view the description of the selected event handler in JSON format. If any changes were applied to a predefined event handler, they are highlighted in the dialog box. You can return the event handler to the predefined state by clicking Reverse Changes in the Changes dialog box. 

 The command is available only if the event handler is inherited—that is, based on a predefined event handlers. 

 Table: Changes Dialog Box You use this dialog box to view the source code of the event handler; the changes are highlighted in red. The dialog box also contains the following buttons. 

 Button Description 

 Reverse Changes Returns the event handler to the predefined state. 

 Close Closes the dialog box. 

### Event Handler Properties Dialog Box 

 This dialog box opens when you click Add New Record on the page toolbar, or when you click the link in the Handler Name column in the table on the page. The list of properties may differ depending on the event handler. 

 Table: Event Handler Properties Dialog Box: Summary Area The Summary area of this dialog box has the following elements. 


<!-- PAGE_BREAK -->
 Event Handlers | 79 

 Element Description 

 Handler Name The system name of the event handler. 

 Display Name The name of the event handler that is displayed in the diagram view of the workflow (see Workflow (Diagram View) for details). 

 Event Source The source object for the event handler. This is the DAC for which the event is raised. 

 This box is displayed if the value in the Event Type box is Triggered from Code. 

 Event Name The name of the event that needs to be handled. 

 This box is displayed if the value in the Event Type box is Triggered from Code. 

 Event Type The type of event for which the event handler is created or modified. 

 This box is read-only if you are modifying an existing event handler. The box can contain one of the following options: 

- _Triggered by Field Change_ 

- _Triggered from Code_ 

 Field Name The names of the fields whose change triggers the event. 

 You can select one field or multiple fields. 

 This box is displayed if the option in the Event Type box is Triggered by Field Change. 

**_Table: Event Handler Properties Dialog Box: Entity to Apply Workflow Section_** 

In this section, you specify how to get the object for which the workflow should be used. 

 Element Description 

 Object from Event A check box that indicates (if selected) that the system should use the primary data view of the graph where the event has been raised. 

 This check box is available only if the DAC on which the event is raised is the same as the primary DAC of the current graph. 

 Parameter from Event A check box that indicates (if selected) that the system should use the view that has been transferred as the event parameter. 

 This check box is available only if the type of the parameter returned by the event coincides with the primary DAC of the current graph. 

 View from Graph A check box that indicates (if selected) that the system should use the view from the graph for the event handler. 

 This check box is available only if the event handler is predefined and if the code for the event handler contains the BQL for obtaining the entity for which the workflow should be used. 


<!-- PAGE_BREAK -->
 Event Handlers | 80 

 Element Description 

 Allow Multiple Entities A check box that indicates (if selected) that the workflow can be used for multiple entities if the BQL has returned multiple entities. If the check box is cleared, the workflow is used for only the first entity. 

 This check box is available only if the event handler is predefined and if the code for the event handler contains the BQL for obtaining the entity for which the workflow should be used. 

 Table: Event Handler Properties Dialog Box: Field Update Tab In the table on the Field Update tab, you add the fields that should be updated aer the event is processed. The fields are updated in the order in which you add them to the table. You can change the order of the listed rows (and thus the corresponding fields) by clicking the row you want to move and then clicking Move Up or Move Down on the table toolbar. The table toolbar includes only standard buttons. For the list of standard buttons, see Table Toolbar. 

 The table contains the following columns. 

 Column Description 

 Active A check box that indicates (if selected) that the field should be updated after the event is processed. 

 Field The name of the field that should be updated. 

 From Schema A check box that indicates (if selected) that field value from the database should be used. 

 New Value The new value to be used for the field. 

 Status The status of the field update. 

 Table: Event Handler Properties Dialog Box: Buttons This dialog box has the following buttons. 

 Button Description 

 OK Closes the dialog box and applies the changes. 

 Cancel Closes the dialog box without applying any changes. 

### Table 

 This table contains the list of event handlers and the basic settings of each of them. The columns of the table are described below. 

 Column Description 

 Handler Name The internal name of the event handler. 

 If you click the name, the Event Handler Properties dialog box is opened, which shows the properties of the selected event handler. 


<!-- PAGE_BREAK -->
 Event Handlers | 81 

**Column Description** 

**Display Name** The name of the event handler that will be displayed on the _Workflow (Diagram View)_ and _Workflow (Tree View)_ pages. 

**Event Type** The type of the event handler. 

 This column can contain one of the following options: 

- _Triggered by Field Change_ : The event that is triggered by field changes on the UI 

- _Triggered from Code_ : The event that is triggered from code. 

**Event Source** The source object for the event handler. This is the DAC for which the event is raised. 

**Event Name/Field Name** The name of the event that needs to be handled or the names of the fields whose change triggers the event, depending on the value in the **Event Type** column. 

**Status** The status of the event handler. 

 The status of the event handler can be one of the following: 

- _Inherited_ : A system event handler that has not been modified 

- _New_ : An event handler that has been created in the customization project 

- _Modified_ : A system event handler that has been modified in the customization     project 


<!-- PAGE_BREAK -->
 Fields | 82 

## Fields 

 Page ID: (AU201060) 

 For a particular screen (that is, a form in Acumatica ERP), you use the Fields page to add existing fields to the customization project and modify the properties of these fields. 

 You open the Fields page by clicking Fields under the screen ID (of the form for which you are modifying the field’s properties) in the navigation pane of the Customization Project Editor. In the name that appears on the page, Fields is preceded by the form ID and then the form name in parentheses. 

### Page Toolbar and More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Command Description 

 Combo Box Values 

 Opens the Combo Box Values dialog box. In this dialog box, you can configure the list of values for fields that are displayed as combo boxes. The command is available only if you have selected this type of field. 

 View Changes Opens the Changes dialog box, where you can view the description of the selected field in JSON format. If any changes have been applied to the predefined field, they are highlighted in the dialog box. You can return the field to the predefined state by clicking Reverse Changes in the Changes dialog box. 

 The View Changes command is available only if the field has the Inherited status. 

 Table: Add Field Dialog Box This dialog box opens when you click Add New Row on the page toolbar. In this dialog box, you can use the elements of the Selection area to narrow the range of the fields listed in the table. You then select the Included check box for each field you want to add and click the appropriate button to add the fields to the page. 

 Element Description 

 The dialog box has a Selection area with the following elements. 

 Container The form container where the box for the field is located. If you select a container in this box, the table lists only the rows of the fields in the container, and the DAC box is filled in automatically with the corresponding DAC. 

 DAC The DAC that contains the field. If you select a DAC in this box, the table narrows the range of listed rows to display the fields of the DAC. 

 Field Name The internal name of the field to be added to the customization project. The system lists the available values of the DAC selected in the DAC box. 


<!-- PAGE_BREAK -->
 Fields | 83 

 Element Description 

 Display Name The read-only name of the field that is selected in the Field Name box. This name will be displayed on the applicable Acumatica ERP form. 

 The dialog box contains a table with the following columns. The table lists the fields that meet any selection criteria you have specified in this dialog box. 

 Included A check box that you can select to add the field to the table on the page. 

 The check box is also selected if the field has already been added to the table. 

 Container The form container where the box for the field is located. 

 DAC The data access class from the container that is selected in the Container box. The system inserts this value automatically if you are manually adding the row. 

 Field Name The internal name of the field that can be added to the customization project. 

 Display Name The name of the field that will be displayed on the applicable Acumatica ERP form. 

 This dialog box has the following buttons. 

 Add Adds the selected field or fields to the table on the page without closing the dialog box. 

 Add & Close Adds the selected field or fields to the table on the page and closes the dialog box. 

 Close Closes the dialog box without adding any fields to the table on the Fields page. 

**_Table: Combo Box Values Dialog Box_** 

This dialog box opens if on the Fields page, you click a field that is displayed as a combo box on the applicable Acumatica ERP form and then you click **Combo Box Values** on the page toolbar. In the dialog box, you can specify or modify the values for the field you have selected. The table toolbar includes only standard buttons. For the list of standard buttons, see _Table Toolbar_. 

 Element Description 

 The dialog box contains the following columns. 

 Active A check box that indicates (if selected) that the current value is active, meaning that it will be available for selection in the combo box on the applicable Acumatica ERP form. 

 Custom A check box that indicates (if selected) that the current value is a user-defined value. 

 The system automatically selects this check box for the values that you add in the dialog box. The check box is read-only for the default system values. 

 Value The internal name of the value. 

 Description The name of the value that will be displayed in the combo box on the applicable Acumatica ERP form. 

 This dialog box has the following buttons. 

 OK Closes the dialog box and applies the changes. 


<!-- PAGE_BREAK -->
 Fields | 84 

 Element Description 

 Cancel Closes the dialog box without applying any changes to the combo box values of the field. 

 Table: Changes Dialog Box You use this dialog box to view the source code of the field; the changes are highlighted in red. The dialog box also contains the following buttons. 

 Element Description 

 Revert Changes Returns the field to its predefined state. 

 Close Closes the dialog box. 

### Table 

 This table contains the list of fields and the basic settings of each of them. The columns of the table are described below. 

 Column Description 

 Object Name The data access class that contains the field. 

 Field Name The internal name of the field. 

 Disabled An indicator of when the field is disabled on the applicable Acumatica ERP form. 

 By default, the column is empty, indicating that the field is always enabled. If the column is not empty, it can contain one of the following: 

- _True_ : The field is always disabled. 

- Condition: The condition that, if it is met, causes the field to be disabled. If any condi-     tions are specified on the _Conditions_ page for the screen of this field, they are available     for selection in this column. 

 Hidden An indicator of when the field is hidden on the applicable Acumatica ERP form. 

 By default, the column is empty, indicating that the field is always visible. If the column is not empty, it can contain one of the following: 

- _True_ : The field is always hidden. 

- Condition: The condition that, if it is met, causes the field to be hidden. If any condi-     tions are specified on the _Conditions_ page for the screen of this field, they are available     for selection in this column. 

 Required An indicator of when the field is marked as required on the applicable Acumatica ERP form. 

 By default, the column is empty, indicating that the field is never required. If the column is not empty, it can contain one of the following: 

- _True_ : The field is always marked as required. 

- Condition: The condition that, if it is met, causes the field to be required. If any con-     ditions are specified on the _Conditions_ page for the screen of this field, they became     available for selection in the box. 


<!-- PAGE_BREAK -->
 Fields | 85 

**Column Description** 

**Display Name** The name of the field that will be displayed on the applicable Acumatica ERP form. 

**From Schema** A check box that indicates (if selected) that field value from the database should be used. 

**Default Value** The value that is displayed for the field by default. 

**Status** The status of the field. 

 The status of the field can be one of the following: 

- _Inherited_ : A system field 

- _New_ : A field that you have added 

- _Modified_ : A system field that you have modified 


<!-- PAGE_BREAK -->
 Generic Inquiries | 86 

## Generic Inquiries 

 Page ID: (AU206000) 

 On this page, you manage the GenericInquiryScreen items in the customization project. A GenericInquiryScreen item contains the dataset of a custom or customized generic inquiry form. 

 You open the Generic Inquiries page by clicking Generic Inquiries in the navigation pane of the Customization Project Editor. 

### Page Toolbar and More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Command Description 

 Manage Inquiries Opens the Generic Inquiry (SM208000) form in a new browser tab. 

 Reload from Database 

 Updates the GenericInquiryScreen items in the customization project if the generic inquiries that correspond to these items have been modified on the Generic Inquiry (SM208000) form. 

 Table: Add Generic Inquiries Dialog Box This dialog box opens when you click Add New Record on the page toolbar. The dialog box displays a table listing all the custom and customized generic inquiries that exist in your instance of Acumatica ERP. The table toolbar includes only standard buttons. For the list of standard buttons, see Table Toolbar. 

 Element Description 

 The dialog box has a table with the following columns. 

 Included A check box that you select to add the current generic inquiry to the customization project. 

 Inquiry Title The name of the generic inquiry as it is displayed on the Generic Inquiry (SM208000) form. 

 Last Modified By The name of the user who last modified the generic inquiry in the customization project. 

 Last Modified On The date when the generic inquiry was last modified in the customization project. 

 This dialog box has the following buttons. 

 Save Adds the selected generic inquiries to the table on the page and closes the dialog box. 

 Cancel Closes the dialog box without adding any generic inquiries to the page. 


<!-- PAGE_BREAK -->
 Generic Inquiries | 87 

 The system automatically includes in the customization project information about the workspace or workspaces to which the generic inquiry has been added on the UI, along with other information about the generic inquiry. 

### Table 

 This table contains the list of generic inquiries and the basic settings of each of them. The columns of the table are described below. 

 Column Description 

 Object Name The name of the generic inquiry in the customization project. 

 Description The description of the generic inquiry. 

 Last Modified By The name of the user who last modified the generic inquiry in the customization project. 

 Last Modified On The date when the generic inquiry was last modified in the customization project. 

 If you delete a GenericInquiryScreen item from the project, the generic inquiry remains in the system unless you delete the inquiry by using the Generic Inquiry (SM208000) form. 


<!-- PAGE_BREAK -->
 Import and Export Scenarios | 88 

## Import and Export Scenarios 

 Page ID: (AU205500) 

 On this page, you manage the XportScenario items in the customization project. An XportScenario item contains the dataset of a custom export or import scenario that is used to perform data migration between a legacy application and Acumatica ERP. 

 You open the Import and Export Scenarios page by clicking Import/Export Scenarios in the navigation pane of the Customization Project Editor. 

### Page Toolbar 

 The page toolbar includes standard and page-specific buttons. For the list of standard buttons, see Page Toolbar. The page-specific buttons are listed below. 

 Command Description 

 Manage Scenarios Opens the Import Scenarios (SM206025) form in a new browser tab. 

 Reload from Database 

 Updates the XportScenario items in the customization project if the integration scenarios that correspond to these items have been modified on the Import Scenarios (SM206025) form. 

 Table: Add Import or Export Scenario Dialog Box This dialog box opens when you click Add New Record on the page toolbar. The dialog box displays all the custom integration scenarios that exist in your Acumatica ERP instance. You can select multiple integration scenarios to add them to the project simultaneously. 

 Element Description 

 The table in the dialog box has the following columns. 

 Selected A check box that you select to add the current integration scenario to the customization project. 

 Name The name of the integration scenario. 

 This dialog box has the following buttons. 

 OK Adds the selected integration scenarios to the table on the page and closes the dialog box. 

 Cancel Closes the dialog box without adding any scenarios to the page. 

 An XportScenario item contains all the data required for the integration scenario. Therefore, the item includes the data of the data provider. 


<!-- PAGE_BREAK -->
 Import and Export Scenarios | 89 

### Table 

 This table contains the list of integration scenarios and the basic settings of each of them. The columns of the table are described below. 

 Column Description 

 Object Name The name of the integration scenario in the customization project. 

 Description The description of the integration scenario. 

 Last Modified By The name of the user who last modified the integration scenario in the customization project. 

 Last Modified On The date when the integration scenario was last modified in the customization project. 


<!-- PAGE_BREAK -->
 Mobile Application | 90 

## Mobile Application 

 Page ID: (AU220000) 

 You use this page to manage the screens of the Acumatica mobile app. 

 You open the Mobile Applications page by clicking Mobile Application in the navigation pane of the Customization Project Editor. 

### Page Toolbar and More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Command Description 

 Add New Screen Opens the Add New Screen dialog box, in which you specify the screen ID and then click OK. 

 The system adds the selected screen to the mobile app, adds the add item to the table on the page, and opens the Add page (see the Pages section of this topic). The system also adds a node for the Add page beneath the Mobile Application node of the navigation pane. 

 Clear All Tenants Reverses the changes to all tenants. 

 Clear Current Tenant Reverses the changes to the current tenant. 

 Manage Workspaces Opens the Mobile Workspaces page. 

 Remove Existing Screen 

 Opens the Remove Existing Screen dialog box, in which you specify the screen ID, and then click OK. 

 When you click OK , the system removes the selected screen from the mobile app and adds the remove item to the table on the page (see the Pages section of this topic). The system also adds a node for the Remove page beneath the Mobile Application node of the navigation pane. You click the node to open the Remove page. 

 Update Existing Screen 

 Opens the Update Existing Screen dialog box, in which you specify the screen ID and then click OK. 

 The system adds the update item to the table on the page and opens the Update page (see the Pages section of this topic). The system also adds a node for the Update page beneath the Mobile Application node of the navigation pane. 

 Update Main Menu Opens the Update Menu page (see the Pages section of this topic), where you can update the main menu of the mobile app. 

 The system adds the update item to the table on the page and opens the Update Menu page (see the Pages section of this topic). The system also adds a node for the Update Menu page beneath the Mobile Application node of the navigation pane. 


<!-- PAGE_BREAK -->
 Mobile Application | 91 

### Table 

 This table contains the list of modified screens and the basic settings of each of them. The columns of the table are described below. 

 Element Description 

 Operation The type of the operation performed with the screen. 

 The column can contain the following values: 

- _add_ 

- _update_ (with the screen ID specified in the **Screen ID** column) 

- _update_ (with the _Menu_ specified in the **Screen ID** column 

- _remove_ 

 Screen ID The ID of the added, modified, or removed screen. 

 Title The name of the screen. 

 Last Modified By The name of the user who last performed the operation in the customization project. 

 Last Modified On The date when the operation was last performed in the customization project. 

### Pages 

 From the Mobile Application page, you can open any of the following pages related to the Acumatica mobile app: 

- Add: By using the Add page, which you open by clicking **Add New Screen** on the Mobile Application page,     you can add a new screen to the Acumatica mobile app. In the name that appears on the page, _Add_ is     followed by a colon, the screen ID, and then the screen name. 

- Remove: You use the Remove page to remove a screen from the Acumatica mobile app. This page is opened     when you click **Remove Existing Screen** on the Mobile Application page. In the name that appears on the     page, _Remove_ is followed by a colon, the screen ID, and then the screen name. 

- Update: You update an existing screen of the Acumatica mobile app by using the Update page. To open this     page, you click **Update Existing Screen** on the Mobile Application page. In the name that appears on the     page, _Update_ is followed by a colon, the screen ID, and then the screen name. 

- Update Menu: You use the Update Menu page, which opens when you click **Update Main Menu** on the     Mobile Application page, to update the main menu of the Acumatica mobile app. The name that appears on     the page is _Update: MENU_. The pages have the same structure, as described below. 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Button Description 

 Export Preview as XML Exports the settings of the page as an XML file. 


<!-- PAGE_BREAK -->
 Mobile Application | 92 

**_Table: Source Code Pane_** 

The Source Code pane consists of the following areas. 

 Area Description 

 Commands The area where you add the instructions to modify the screen. 

 Errors The area that displays any errors that are generated. 

 Result Preview The area that displays the code of the updated screen configuration. 


<!-- PAGE_BREAK -->
 Mobile Workspaces | 93 

## Mobile Workspaces 

 Form ID: (AU220012) 

 On this page, you manage the workspaces of the Acumatica mobile app by using the following type of items. 

- _MobileSitemapWorkspace_ : An item of this type contains general data, such as the name of a workspace, its     sequential number, and its icon. 

- _MobileSitemapWorkspaceItems_ : An item of this type contains the screens included in the workspace. 

- _MobileSitemapWorkspaceWidgets_ : An item of this type contains the KPI widgets included in the workspace     and its screens. 

 You open the Mobile Workspaces page by clicking Manage Workspaces on the page toolbar of the Mobile Application page. 

### Page Toolbar and More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Command Description 

 Manage Workspaces 

 Opens the Mobile Workspaces (AU220012) form in a new browser tab. You can use this form to manage workspaces for the Acumatica mobile app. 

 Reload from Database 

 Updates the MobileSitemapWorkspace , MobileSitemapWorkspaceItems , and MobileSitemapWorkspaceWidgets items in the customization project if the data that corresponds to these items has been modified on the Mobile Workspaces (AU220012) form. 

 Table: Add Workspace Dialog Box This dialog box, which opens when you click Add New Record on the page toolbar, has a table that lists the workspaces that have been created on the Mobile Workspaces (AU220012) form. The dialog box contains the following elements. 

 Element Description 

 The table toolbar includes only standard buttons. For the list of standard buttons, see Table Toolbar. 

 The dialog box has the following columns. 

 Included A check box that indicates (if selected) that the workspace in this row will be added to the customization project if you click Save in the dialog box. 

 Workspace ID The internal name of the workspace. 

 Display Name The name of the workspace as it is displayed in the mobile app. 

 Icon The icon that is displayed for this workspace in the mobile app. 

 Active A check box that indicates (if selected) that the current workspace is active—that is, it will be displayed in the mobile app. 


<!-- PAGE_BREAK -->
 Mobile Workspaces | 94 

 Element Description 

 This dialog box has the following buttons. 

 Save Adds the selected workspaces to the table on the page and closes the dialog box. 

 Cancel Closes the dialog box without any changes. 

### Table 

 This table contains the list of workspaces in the customization project and the basic settings of each of them. The columns of the table are described below. 

 Column Description 

 Object Name The name of the workspace in the customization project. 

 Description The description of the workspace. 

 Last Modified By The name of the user who last modified the workspace in the customization project. 

 Last Modified On The date when the workspace was last modified in the customization project. 


<!-- PAGE_BREAK -->
 Modern UI Editor | 95 

## Modern UI Editor 

 Page ID: (AU201080) 

 You use this page to customize the original HTML code of a form and to automatically create a new extension file that contains the customized HTML code. 

 You open the Modern UI Editor page by expanding the Screens node in the navigation pane of the Customization Project Editor. In the list of forms displayed under the expanded Screens node, expand the node that corresponds to the form whose HTML code you want to customize, and click the Modern UI Editor node. 

### Page Toolbar 

 The page toolbar includes only the page-specific buttons listed in the following table in alphabetical order. 

 Button Description 

 Compare HTML Opens the Compare HTML dialog box, which shows the code changes you have made. If you specify a value in the Extension Suffix box and click OK , the system will create the extension file (with the specified suffix appended) based on your code changes. The system generates the extension file in the extensions folder in the FrontendSources\screen\src\customizationScreens\<Tenant Name>\screens\<FirstTwoLettersOfFormID>\<FormID>\ file path of your Acumatica ERP instance. 

 Reload Original HTML Discards all changes you have made to the HTML code of the form and reloads the original code in the HTML editor. 

### HTML Editor 

 You use the HTML editor of the Modern UI page to view and edit the HTML code of a form that you want to customize. You can then click Compare HTML to begin the process of generating the extension file. 


<!-- PAGE_BREAK -->
 Project XML Editor | 96 

## Project XML Editor 

 You use the Project XML Editor to edit and review the content of a customization project in XML format. 

 You open the editor by clicking File > Edit Project XML on the main menu of the Customization Project Editor. The actual name shown on the page is the name of the customization project. 

### Page Toolbar 

 The page toolbar contains the name of the customization project and the following buttons. 

 Button Description 

 Choose File Opens the standard dialog box, in which you select a deployment package file. The deployment package is a ZIP file that has the same name as the customization project. 

 Download Package Saves the project locally as a deployment package. 

 Save to Database Saves the XML code of the project to the database. 

 Upload Package Opens the deployment package file that has been selected; the name of the file is displayed on the page toolbar. 

 You click this button after you select the deployment package file by clicking Choose File. 

### Source Code Pane 

 You use this pane of the page to view and edit the contents of the customization project. 


<!-- PAGE_BREAK -->
 Push Notifications | 97 

## Push Notifications 

 Page ID: (AU210000) 

 On this page, you manage the PushNotification items in the customization project. A PushNotification item contains the dataset of a push notification definition. A push notification definition includes the push notification destination and the data query, which defines the data changes for which Acumatica ERP sends notifications. 

 You open the Push Notifications page by clicking Push Notifications in the navigation pane of the Customization Project Editor. 

### Page Toolbar and More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Command Description 

 Manage Notifications 

 Opens the Push Notifications (SM302000) form in a new browser tab. 

 Reload from Database 

 Updates the PushNotification items in the customization project if the push notifications that correspond to these items have been modified on the Business Events (SM302050) form. 

 Table: Add Push Notifications Dialog Box This dialog box opens when you click Add New Record on the page toolbar. The dialog box displays all the push notification definitions that are configured in your instance of Acumatica ERP.The dialog box contains the following elements. The table toolbar includes only standard buttons. For the list of standard buttons, see Table Toolbar. 

 Element Description 

 Included A check box that indicates (if selected) that the current push notification will be added to the customization project. 

 Destination Name The name of the notification destination. 

 Destination Type The type of the notification destination. 

 This dialog box has the following buttons. 

 Save Adds the selected business events to the table on the page and closes the dialog box. 

 Cancel Closes the dialog box without making any changes. 


<!-- PAGE_BREAK -->
 Push Notifications | 98 

### Table 

 This table contains the list of push notifications and the basic settings of each of them. The columns of the table are described below. 

 Column Description 

 Object Name The name of the push notification in the customization project. 

 Description The description of the push notification. 

 Last Modified By The name of the user who last modified the push notification in the customization project. 

 Last Modified On The date when the push notification was last modified in the customization project. 

 If you delete a PushNotification item from the project, the push notification definition remains in the system unless it is deleted on the Push Notifications (SM302000) form. 


<!-- PAGE_BREAK -->
 Reports | 99 

## Reports 

 Page ID: (AU207000) 

 On this page, you manage the Report items in the customization project. A Report item contains the dataset of a custom report created with Acumatica Report Designer. 

 You open the Reports page by clicking Reports in the navigation pane of the Customization Project Editor. 

### Page Toolbar and More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Command Description 

 Reload from Database 

 Updates the Report items in the customization project if the reports that correspond to these items have been modified in the Report Designer. 

 Table: Select Report from Database Dialog Box This dialog box opens when you click Add New Record on the page toolbar. Before adding a report to a project, you have to construct the report in the Report Designer and save the report to the database. (For more information about reports, see Acumatica Report Designer Guide .) The dialog box contains the following elements. 

 The table toolbar includes only standard buttons. For the list of standard buttons, see Table Toolbar. 

 Element Description 

 Name The name of the report. 

 If a custom report is created in the Report Designer and saved as a file in the file system, you cannot add the report to a customization project as a Report item. 

 This dialog box has the following buttons. 

 Save Adds the selected report to the table on the page and closes the dialog box. 

 Cancel Closes the dialog box without making any changes. 

### Table 

 This table contains the list of custom reports and the basic settings of each of them. The columns of the table are described below. 


<!-- PAGE_BREAK -->
 Reports | 100 

**Column Description** 

**Object Name** The name of the report in the customization project. 

**Description** The description of the report. 

**Last Modified By** The name of the user who last modified the report in the customization project. 

**Last Modified On** The date when the report was last modified in the customization project. 


<!-- PAGE_BREAK -->
 Screen Editor | 101 

## Screen Editor 

 Page ID: (AU204520) 

 The Screen Editor page is the visual editor for the source code of an ASPX page and the business logic of a screen. You use this page to configure ASP.NET containers (such as forms and grids), and to specify the properties of UI controls and grids. 

 You can open the Screen Editor page in a variety of ways, including by clicking the screen ID (of the form you want to customize in the navigation pane of the Customization Project Editor. You can also open it from other pages, such as Customized Screens page. In the actual name that appears on the page, Screen Editor: is followed by the form ID of the form being customized and then the form name in parentheses. 

### Page Toolbar and More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Command Description 

 Customize Business Logic 

 Opens the Code Editor page with the extension class template of the business logic container (BLC) that is bound to the form. 

 Customize Data Class Opens the Data Class page for customization of the DAC that contains the field selected in the control tree. 

 Edit Aspx Opens the ASPX Editor page with the webpage source code. 

 Open Screen Opens the original form of Acumatica ERP. 

 Preview Changes Opens the customized form in a new browser window. 

### Control Tree 

 The control tree of the Screen Editor contains a list of the elements that are displayed on the form and the layout rules that organize the elements into rows and columns. (You can see the list of controls that can be added to a form on the Add Controls tab of the Screen Editor.) 

 The toolbar of the control tree includes the following buttons. 

 Button Description 

 Refresh Refreshes the control tree. 

 Remove Removes the item selected in the control tree from the form. 

 Reset Properties Resets all controls and actions to the out-of-the-box state. 


<!-- PAGE_BREAK -->
 Screen Editor | 102 

### Layout Properties Tab 

 On the Layout Properties tab, you review and modify the layout properties of the form controls or actions that are defined on the ASPX page. 

 The tab contains a table toolbar and a table. The table toolbar includes the Hide Advanced Properties button ( ), which you can use to hide or show the advanced properties of the selected control. The tab table consists of the following columns. 

 Column Description 

 Override A check box that indicates whether the property value has been changed. This check box is selected automatically when you change the property value. 

 Property The name of the property or the property group. 

 Value The value of the property. 

### Attributes Tab 

 You use the Attributes tab to review and customize the attributes of the DAC field that is bound to the control currently selected in the control tree. The tab consists of elements that hold the DAC field information and buttons to customize the field attributes. 

 Table: Attributes Elements The tab contains the following elements. 

 Element Description 

 Data Class The name of the DAC to which the field belongs. 

 Field Name The name of the field in the DAC. The field name is the name of the public virtual property in the public abstract class of the field. 

 Original Attributes The original attributes of the field in Acumatica ERP. 

 Table: Attributes Buttons The tab has the following buttons. 

 Button Description 

 Customize Attributes 

 Opens the Data Class page so you can customize the field attributes in the DAC. 

 View Source Opens the Data Access tab of the Source Code (SM204570) form so that you can browse the DAC source code. 

 Override on Screen Level 

 Opens the Code Editor page with the BLC extension class template. The template includes the field attributes and the template of the DACName_FieldPropertyName_CacheAttached() method, which you can use to replace the attributes within the BLC. 


<!-- PAGE_BREAK -->
 Screen Editor | 103 

### Events Tab 

 On the Events tab, you view and add event handlers for the selected control. 

 The tab consists of summary elements and a table (which has a toolbar). 

 Table: Events Elements The tab contains the following elements. 

 Element Description 

 Data Class The name of the DAC to which the field belongs. 

 Field Name The name of the field in the DAC. 

 Business Logic The name of the BLC bound to the form. 

 Table: Table Toolbar The table toolbar includes the following table-specific buttons. 

 Button Description 

 Add Handler For the selected event (that is, the event that you have clicked in the table), opens the Code Editor page with the BLC extension class template. The class template includes a code template for the event handler, so you should implement only the body of the handler. 

 The button provides the following menu commands: 

- **Keep Base Method** : Creates the event handler with two parameters, as it is defined in     the base BLC. As a result, the event handler is added to the appropriate event handler     collection. 

- **Override Base Method** : Creates the event handler with an additional parameter to re-     place the base BLC event handler collection. 

 View Source Opens the Source Code browser with the source code of the BLC bound to the form. 

 Table: Table Columns The table holds information about the event handlers used for the selected control. It contains the following columns. 

 Column Description 

 Event The event name. 

 Handled in Source A check box that indicates whether the event handler is implemented within Acumatica ERP. 

 Customized A check box that indicates whether the event handler is customized. This check box is selected automatically when you add the event handler. 


<!-- PAGE_BREAK -->
 Screen Editor | 104 

### Add Control Tab 

 You can use the Add Control tab to easily add new containers, controls, and layout rules to the form you are modifying. The tab has the Main Containers , Layout Rules , and Other Controls sections with rectangles for the types of controls in the sections. 

 The Main Containers section has rectangles for each of the following controls, which you can add: Form , Tab , Tab Item , Grid , and Pop-Up Panel. 

 The Layout Rules section has rectangles for each of the following controls, which you can add: Row , Column , Group , Merge , and Empty Rule. 

 The Other Controls section has rectangles for each of the following controls, which you can add: Panel , Group Box , Radio Button , Label , Button , and Java Script. 

 To add a control, you drag its box from this tab to the needed position in the control tree. Aer you have added the control, you specify its properties on the Layout Properties tab. 

### Add Data Fields Tab 

 You use the Add Data Fields tab to manage the controls in the form container that is currently selected in the control tree. On this tab, you can create a control for a DAC field and add it to the selected container. You can also create a new custom field in a DAC, create a control for the field, and add it to the selected container. 

 The tab contains the Data View drop-down list and a table with a table toolbar and three filters you can use to view the needed fields. 

 Table: Add Data Fields Element The tab contains the following element. 

 Element Description 

 Data View The DAC whose fields you want to view in the table. The drop-down list includes all DACName(DataViewName) pairs of the BLC that are bound to the form. 

 Table: Table Toolbar The table toolbar has the following buttons. 

 Button Description 

 Create Controls Adds the selected fields (that is, those for which you have selected the unlabeled Included check boxes in the table) to the container selected in the control tree. 

 New Field Opens the Create New Field Dialog Box , which you can use to add a new custom field to the DAC that is referenced in the data view selected in the Data View box. 

 Once you have created a field or multiple fields, you need to publish the customization project before you can create a control for the new fields. 

 Table: Table Columns This table displays the fields that belong to the selected DAC. The table includes the following columns. 


<!-- PAGE_BREAK -->
 Screen Editor | 105 

 Column Description 

 Included An unlabeled check box that you use to include this field in processing when you click Create Controls on the table toolbar. This processing will create a control for the field in the container that is currently selected in the control tree. 

 Used Read-only. A check box that indicates whether a control for the field exists in the object that is currently selected in the control tree. The system selects this check box automatically when you create a control for the field. 

 Field Name The name and DisplayName (in parentheses) of the field in the DAC. 

 Control The type of the UI control. 

 Table: Filter Tabs You can use the following filter tabs to select which DAC fields you want to display in the table. 

 Filter Description 

 All All fields of the selected DAC that are not represented by controls on the form. 

 Visible The fields that are visible because of the Visibility field attribute in the selected DAC. 

 Custom The new custom fields of the selected DAC. 

### View ASPX Tab 

 The View ASPX tab displays the ASPX code of the control selected in the control tree. 


<!-- PAGE_BREAK -->
 Shared Filters | 106 

## Shared Filters 

 Page ID: (AU205100) 

 On this page, you manage the SharedFilter items in the customization project. A SharedFilter item contains the dataset of a custom reusable shared filter created on a processing or inquiry form of Acumatica ERP. 

 You open the Shared Filters page by clicking Shared Filters in the navigation pane of the Customization Project Editor. 

### Page Toolbar and More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Command Description 

 Manage Filters Opens the Filters (CS209010) form in a new browser tab. 

 Reload from Database 

 Updates the SharedFilter items in the customization project if the shared filters that correspond to these items have been modified on the Filters (CS209010) form or on the form to which the filter is applied. 

 Table: Add Shared Filter Dialog Box This dialog box opens when you click Add New Record on the page toolbar. The dialog box lists all the custom shared filters that exist in your instance of Acumatica ERP. You can select multiple shared filters to add them to the customization project simultaneously. The dialog box contains the following elements. 

 Element Description 

 The table in this dialog box has the following columns. 

 Selected A check box that you select to add the current filter to the customization project. 

 Name The name of the shared filter. 

 User Name The user who created the shared filter. 

 Screen ID The ID of the form on which the shared filter has been created. 

 This dialog box has the following buttons. 

 OK Adds the selected shared filters to the table on the page and closes the dialog box. 

 Cancel Closes the dialog box without making any changes on the page. 


<!-- PAGE_BREAK -->
 Shared Filters | 107 

### Table 

 This table contains the list of shared filters and the basic settings of each of them. The columns of the table are described below. 

 Column Description 

 Object Name The name of the shared filter in the customization project. 

 Description The description of the shared filter. 

 Last Modified By The name of the user who last modified the shared filter in the customization project. 

 Last Modified On The date when the shared filter was last modified in the customization project. 


<!-- PAGE_BREAK -->
 Site Map | 108 

## Site Map 

 Page ID: (AU208000) 

 On this page, you manage the SiteMapNode items in the customization project. A SiteMapNode item contains the dataset of a custom site map node for a custom form or report included in the customization project. The item also includes information about the location of the form or report on the UI (such as the workspace or workspaces in which the form or report is included). 

 You open the Site Map page by clicking Site Map in the navigation pane of the Customization Project Editor. 

### Page Toolbar and More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Command Description 

 Manage Site Map Opens the Site Map (SM200520) form in a new browser tab. 

 Reload from Database 

 Updates the SiteMapNode items in the customization project if the site map nodes that correspond to these items have been modified on the Site Map (SM200520) form. 

 Table: Add Site Map Items Dialog Box This dialog box opens when you click Add New Record on the page toolbar. The dialog box displays all the custom site map nodes that have been created in the site map of Acumatica ERP, and the nodes that have been modified in the site map. You can select multiple custom site map nodes to add them to the project simultaneously. The dialog box contains the following elements. 

 Element Description 

 The table toolbar includes only standard buttons. For the list of standard buttons, see Table Toolbar. 

 The table in this dialog box has the following columns. 

 Included A check box that you select to add the current site map node to the customization project. 

 Screen ID The screen ID associated with the site map node. 

 Title The screen name as it is displayed on the form in Acumatica ERP. 

 Last Modified On The date when the site map node was last modified in the customization project. 

 This dialog box has the following buttons. 

 Save Adds the selected site map nodes to the table on the page and closes the dialog box. 

 Cancel Closes the dialog box without making any changes on the page. 


<!-- PAGE_BREAK -->
 Site Map | 109 

### Table 

 This table contains the list of site map nodes and the basic settings of each of them. The columns of the table are described below. 

 Column Description 

 Object Name The name of the site map node in the customization project. 

 Description The description of the site map node. 

 Last Modified By The name of the user who last modified the site map node in the customization project. 

 Last Modified On The date when the site map node was last modified in the customization project. 


<!-- PAGE_BREAK -->
 Source Code | 110 

## Source Code 

 Form ID: (SM204570) 

 You use this form, which functions as a source code browser, to explore the source code of Acumatica ERP. 

 The source code browser displays the code in various views on each of the tabs, which are described in the following sections. 

### Screen ASPX Tab 

 You use this tab to view the ASPX code for the selected form. The tab contains the following element. 

 Element Description 

 Screen ID The ID of the form whose source code you want to view. 

 In this box, you can find a form by its ID or its title. You can search by any part of the ID or title. 

 The tab also contains the Source Code pane, which displays the source code of the selected form. The source code is displayed with the changes that were made in all the published customization projects of the website. The changes related to the UI elements of the page are highlighted in yellow. 

### Screen HTML Tab 

 You use this tab to view the HTML code for the selected form. The tab contains the following element. 

 Element Description 

 Screen ID The ID of the form whose source code you want to view. 

 In this box, you can find a form by its ID or its title. You can search by any part of the ID or title. 

 The tab also contains the Source Code pane, which displays the source code of the selected form. The source code is displayed with the changes that were made in all the published customization projects of the website. 

### Screen TypeScript Tab 

 You use this tab to view the TypeScript code for the selected form. The tab contains the following element. 

 Element Description 

 Screen ID The ID of the form whose source code you want to view. 

 In this box, you can find a form by its ID or its title. You can search by any part of the ID or title. 

 The tab also contains the Source Code pane, which displays the source code of the selected form. The source code is displayed with the changes that were made in all the published customization projects of the website. 


<!-- PAGE_BREAK -->
 Source Code | 111 

### Business Logic Tab 

 This tab displays the source code of the BLC. If you selected a form on the Screen ASPX tab, this tab opens with the source code of the graph associated with the form; you can select another graph. If you did not select a form, this tab is empty. 

 The tab contains the following element. 

 Element Description 

 Graph Name The name of the graph for which you want to view the source code. 

 In this box, you can select the graph by its name. You can also type any part of the name and select the name from the list of names that match your search string. 

 The tab contains a navigation pane. The pane has the Methods and Event Handler headers, which are followed by the methods and event handlers (respectively) for the selected graph. You click a particular method or event handler name to view its code in the Source Code pane of the tab. 

 The Source Code pane displays the whole source code of the selected graph. When you click a particular method or event handler in the navigation pane, the system scrolls to the code for this method or event handler. 

### Data Access Tab 

 You use the Data Access tab to review the source code of a DAC. The tab contains the following element. 

 Element Description 

 Table Name The name of the DAC. 

 In this box, you can type any part of the class name and select the name from the list of names that match your search string. 

 The tab also contains the Source Code pane, which displays the source code of the DAC selected in the Table Name box. 

### Find in Files Tab 

 You use this tab to search for Acumatica ERP application code fragments that contain the specified text. The search is case-sensitive. 

 The tab contains the following elements. 

 Element or Pane Description 

 The Summary area contains the following elements. 

 Find Text A box where you enter a fragment of the source code you need to find. 

 Find A button that you click to start the search. 

 Table: Table Columns The table on the tab contains the results of the search. 


<!-- PAGE_BREAK -->
 Source Code | 112 

 Column Description 

 Name The name of the source code file that has been found. 

 Line The number of the code line (in the source code file) that contains the code fragment. 

 Content The contents of the line in the source code file. 

The tab also contains the Source Code pane that displays the code of the item selected in the table. You click a row in the table to view the corresponding source code. 


<!-- PAGE_BREAK -->
 System Locales | 113 

## System Locales 

 Page ID: (AU205000) 

 On this page, you manage the Locale items in the customization project. A Locale item contains the dataset of a system locale, which is a set of parameters that defines the language and other local preferences—such as how to display numbers, dates, and times in the user interface—for a group of users. 

 You open the System Locales page by clicking System Locales in the navigation pane of the Customization Project Editor. 

### Page Toolbar and More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Command Description 

 Manage Locales Opens the System Locales (SM200550) form in a new browser tab. 

 Reload from Database 

 Updates the Locale items in the customization project if the system locales that correspond to these items have been modified on the System Locales (SM200550) form. 

 Table: Add Locale Dialog Box This dialog box opens when you click Add New Record on the page toolbar. The dialog box contains a table that displays all the system locales that exist in your instance of Acumatica ERP. You can select multiple system locales to add them to the project simultaneously. The dialog box contains the following elements. 

 Element Description 

 The table toolbar includes only standard buttons. For the list of standard buttons, see Table Toolbar. 

 The dialog box has the following columns. 

 Selected A check box that you select to add the current system locale to the customization project when you click OK. 

 Locale Name The internal name of the system locale. 

 Locale Name in Locale Language 

 The name of the system locale as it is displayed on the Acumatica ERP forms. 

 This dialog box has the following buttons. 

 OK Adds the selected system locales to the table on the page and closes the dialog box. 

 Cancel Closes the dialog box without making any changes on the page. 


<!-- PAGE_BREAK -->
 System Locales | 114 

### Table 

 This table contains the list of system locale and the basic settings of each of them. The columns of the table are described below. 

 Column Description 

 Object Name The name of the system locale in the customization project. 

 Description The description of the system locale. 

 Last Modified By The name of the user who last modified the system locale in the customization project. 

 Last Modified On The date when the system locale was last modified in the customization project. 


<!-- PAGE_BREAK -->
 Tables to Track Deleted Records | 115 

## Tables to Track Deleted Records 

 Page ID: (AU206005) 

 You use this page to include in a customization project the list of data access classes (DACs) for which the system tracks the removed records. 

 For details about the tracking of removed records, see Tracking Removed Records for Synchronization. 

 You open the Tables to Track Deleted Records page by clicking Tables to Track Deleted Records in the navigation pane of the Customization Project Editor. 

### Page Toolbar and More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Command Description 

 Manage Tables Opens the Tables to Track Deleted Records (SM207010) form in a new browser tab. 

 Table: Add Tables Dialog Box This dialog box, which you use to add data access classes (DACs) to the customization project, opens when you click Add New Record on the page toolbar. The dialog box lists all the DACs that are listed on the Tables to Track Deleted Records (SM207010) form. You need to select the unlabeled Included check boxes for the DACs you want to add. 

 Element Description 

 The dialog box contains the following columns. 

 Included A check box that you select to add the DAC to the customization project. You need to list the DACs on the Tables to Track Deleted Records (SM207010) form first in order they are available for selection. 

 Table The name of the DAC. 

 This dialog box has the following buttons. 

 OK Adds the selected DACs to the table on the page (if they have not already been added) and closes the dialog box. 

 Cancel Closes the dialog box without any changes. 

### Table 

 This table lists the DACs included in the customization project. The table contains the following columns. 


<!-- PAGE_BREAK -->
 Tables to Track Deleted Records | 116 

**Column Description** 

**Object Name** The name of the item that corresponds to the DAC in the customization project. 

**Description** The description of the item that corresponds to the DAC. 

**Last Modified By** The name of the user who last modified the item that corresponds to the DAC in the customization project. 

**Last Modified On** The date when the item that corresponds to the DAC was last modified in the customization project. 


<!-- PAGE_BREAK -->
 User-Defined Fields | 117 

## User-Defined Fields 

 Page ID: (AU230000) 

 On this page, you manage the user-defined fields in the customization project. 

 Any user-defined fields you add on this page are added to the current customization project with all other items. 

 You open the User-Defined Fields page by clicking User-Defined Fields in the navigation pane of the Customization Project Editor. 

### Page Toolbar and More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Command Description 

 Manage User-Defined Fields 

 Opens the Attributes (CS205000) form in a new browser tab so that you can view and change, if needed, the settings of the attributes used for user-defined fields. 

 Reload from Database 

 Updates the properties of user-defined fields in the customization project if these fields have been modified on the Attributes (CS205000) form. 

 Table: Add User-Defined Fields Dialog Box This dialog box opens when you click Add New Record on the page toolbar. The dialog box contains the following elements. The table toolbar includes only standard buttons. For the list of standard buttons, see Table Toolbar. 

 Element Description 

 Included A check box that indicates (if selected) that the user-defined field in this row will be added to the customization project. 

 Attribute ID The attribute that corresponds to the user-defined field. 

 Description The description of the user-defined field. 

 This dialog box has the following buttons. 

 Save Adds the selected user-defined fields to the table on the page and closes the dialog box. 

 Cancel Closes the dialog box without adding any fields. 

 Table: Edit Attribute Dialog Box This dialog box opens when you click Edit on the page toolbar, or when you click the link with the ID of a userdefined field in the Attribute ID column on the page. In the dialog box, you select the IDs of the forms on which the field should appear aer you publish the customization project. You can see only the IDs of the screens for 


<!-- PAGE_BREAK -->
 User-Defined Fields | 118 

 which the user-defined field was added in your Acumatica ERP instance. To add a user-defined field to a form, click Customization > Manage User-Defined Fields on the title bar of the Acumatica ERP form, and add the field. 

 Element Description 

 The table toolbar includes only standard buttons. For the list of standard buttons, see Table Toolbar. 

 The table has the following columns. 

 Included A check box that indicates (if selected) that the user-defined field will be available on the form with the ID specified in the Screen ID column after you publish the customization project. 

 Screen ID The ID of the form on which the user-defined field has been added in your Acumatica ERP instance. 

 This dialog box has the following buttons. 

 Save Adds to the customization project the IDs of the forms for which the user-defined field should be added, and closes the dialog box. 

 Cancel Closes the dialog box without any changes. 

### Table 

 This table contains the list of user-defined fields that you have added to the customization project and the basic settings of each of them. When you click the link in the Attribute ID column, the Edit Attribute dialog box is opened. The columns of the table are described below. 

 Column Description 

 Attribute ID The name of the business event in the customization project. 

 Description The description of the business event. 

 Screen ID The IDs of the forms on which the user-defined field will be available after you publish the customization project. 

 Last Modified By The name of the user who last modified the business event in the customization project. 

 Last Modified On The date when the business event was last modified in the customization project. 


<!-- PAGE_BREAK -->
 Webhooks | 119 

## Webhooks 

 Page ID: (AU210020) 

 On this page, you manage the webhooks in the customization project. 

 You open the Webhooks page by clicking Webhooks in the navigation pane of the Customization Project Editor. 

### Page Toolbar and More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Command Description 

 Manage Webhooks Opens the Webhooks (SM304000) form in a new browser tab so that you can open and modify any webhook. 

 Reload from Database 

 Updates the properties of the webhooks in the customization project if these webhooks have been modified on the Webhooks (SM304000) form. 

 Table: Add Webhooks Dialog Box This dialog box opens when you click Add New Record on the page toolbar. In the dialog box, you can see the names of the webhooks that have been configured on the Webhooks (SM304000) form. 

 Element Description 

 The table toolbar includes only standard buttons. For the list of standard buttons, see Table Toolbar. 

 The table has the following columns. 

 Included A check box that indicates (if selected) that the current webhook will be added to the customization project. 

 Webhook Name The name of the webhook. 

 Implementation Class 

 The implementation class of the webhook. 

 This dialog box has the following buttons. 

 OK Adds the selected webhooks to the table on the page and closes the dialog box. 

 Cancel Closes the dialog box without any changes. 

### Table 

 This table contains the list of webhooks and the basic settings of each of them. The columns of the table are described below. 


<!-- PAGE_BREAK -->
 Webhooks | 120 

**Column Description** 

**Predefined** A check box that indicates (if selected) that the implementation class of the webhook will not be available for editing in the instance where the customization project is published. 

**Object Name** The name of the webhook in the customization project. 

**Implementation Class** 

 The implementation class of the webhook. 

**Description** The description of the webhook. 

**Last Modified By** The name of the user who last modified the webhook in the customization project. 

**Last Modified On** The date when the webhook was last modified in the customization project. 


<!-- PAGE_BREAK -->
 Web Service Endpoints | 121 

## Web Service Endpoints 

 Page ID: (AU206002) 

 On this page, you manage the EntityEndpoint items in the customization project. An EntityEndpoint item contains the dataset of a custom contract-based web service endpoint. 

 You open the Web Service Endpoints page by clicking Web Service Endpoints in the navigation pane of the Customization Project Editor. 

### Page Toolbar and More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Command Description 

 Manage Endpoints Opens the Web Service Endpoints (SM207060) form in a new browser tab. 

 Reload from Database 

 Updates the EntityEndpoint items in the customization project if the web service endpoints that correspond to these items have been modified on the Web Service Endpoints (SM207060) form. 

 Table: Add Entity Endpoint Dialog Box This dialog box opens when you click Add New Record on the page toolbar. The Add Entity Endpoint dialog box displays all the custom contract-based web service endpoints that exist in your Acumatica ERP instance. (System endpoints are not displayed in the dialog box.) You can select multiple endpoints to add them to the project simultaneously. 

 Element Description 

 The table toolbar includes only standard buttons. For the list of standard buttons, see Table Toolbar. 

 The table has the following columns. 

 Included A check box that indicates (if selected) that the web service endpoint in this row will be added to the customization project if you click Save in the dialog box. 

 Endpoint Version The endpoint version. 

 Endpoint Name The name of the web service endpoint. 

 This dialog box has the following buttons. 

 Save Adds the selected web service endpoints to the table on the page and closes the dialog box. 

 Cancel Closes the dialog box without adding any new endpoints. 


<!-- PAGE_BREAK -->
 Web Service Endpoints | 122 

### Table 

 This table contains the list of custom contract-based web service endpoints and the basic settings of each of them. The table contains the following columns. 

 Column Description 

 Object Name The name and version of the web service endpoint in the customization project. 

 Description The description of the web service endpoint. 

 Last Modified By The name of the user who last modified the web service endpoint in the customization project. 

 Last Modified On The date when the web service endpoint was last modified in the customization project. 


<!-- PAGE_BREAK -->
 Wikis | 123 

## Wikis 

 Page ID: (AU206001) 

 On this page, you manage the WikiArticle items in the customization project. A WikiArticle item contains the dataset of a custom wiki and all the articles created within this wiki. 

 You open the Wikis page by clicking Wikis in the navigation pane of the Customization Project Editor. 

### Page Toolbar and More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Command Description 

 Manage Wikis Opens the Wiki (SM202005) form in a new browser tab, so that you can specify the wikis that should be added to the customization project. 

 Reload from Database 

 Updates the WikiArticle items in the customization project if the wikis that correspond to these items have been modified on the Wiki (SM202005) form. 

 Table: Add Wiki Page Dialog Box This dialog box opens when you click Add New Record on the page toolbar. The dialog box displays all the custom wikis that exist in your Acumatica ERP instance. You can select multiple wikis to add them to the project simultaneously. The dialog box contains the following elements. 

 Element Description 

 The table toolbar includes only standard buttons. For the list of standard buttons, see Table Toolbar. 

 The table in the dialog box includes the following columns. 

 Included A check box that you select to add the current wiki to the customization project if you click Save. 

 Name The unique identifier of the wiki. 

 Title The name of the wiki as it is displayed in your Acumatica ERP instance. 

 Last Modified By The name of the user who last modified the wiki. 

 Last Modified On The date when the wiki was last modified. 

 This dialog box has the following buttons. 

 Save Adds the selected wikis to the table on the page and closes the dialog box. 


<!-- PAGE_BREAK -->
 Wikis | 124 

 Element Description 

 Cancel Closes the dialog box without making any changes. 

### Table 

 This table contains the list of wikis that have been added to the customization project, and the basic settings of each of them. The columns of the table are described below. 

 Column Description 

 Object Name The name of the wiki in the customization project. 

 Description The description of the wiki. 

 Last Modified By The name of the user who last modified the wiki in the customization project. 

 Last Modified On The date when the wiki was last modified in the customization project. 


<!-- PAGE_BREAK -->
 Workflow (Diagram View) | 125 

## Workflow (Diagram View) 

 Page ID: (AU201030) 

 For a customized or custom workflow of a particular screen (that is, a form in Acumatica ERP), you can use the diagram view of the Workflow page (also referred to as the Workflow Visual Editor ) to define the states, transitions, and actions of a workflow. (In addition to the diagram view of the workflow, you can use the tree view of the workflow, which is described in Workflow (Tree View) .) The diagram view provides visual representations of the states and the transitions between them. 

 To access the diagram view, you click Diagram View on the page toolbar of the Workflow (Tree View) page for the particular customized, custom, or predefined workflow. The name that appears on the page consists of the form ID, the form name in parentheses, and State Diagram: <Workflow Name> Workflow. (This name is also used for the tree view of the workflow.) 

 For a workflow with composite states, the Workflow Visual Editor is not available, and the Diagram View button is not displayed on the More menu of the Workflow (Tree View) page. 

### Elements of the Diagram View 

 The diagram view of the Workflow page (that is, the Workflow Visual Editor) contains the following parts: 

- The page toolbar and More menu with various buttons and commands. 

- The main area, which displays the workflow of the selected form as a diagram and has the following     elements: 

- Boxes that contain the names of the states of the entity created by using the form and labels with the     names of the actions or event handlers that trigger the transitions. The labels appear aer you create a     transition and specify the source and target states. For example, in the screenshot below, the _New_ box     reflects this state for an opportunity, and the _Open_ and _Close as Won_ labels within this box reflect the     actions a user can perform while the opportunity has the _New_ state (which is the status on the form). 

 Actions and event handlers for the current state are not displayed if they do not trigger any transitions. 

- Arrows that show the transitions between the states. For example, Item 1 in the following screenshot     shows an arrow that represents a transition from the _Won_ state to the _Open_ state of an opportunity that     has been created on the _Opportunities_ (CR304000) form. 

- Buttons that are shown to the right of the diagram: **Zoom In** or **Zoom Out** (see Item 2 in the following     screenshot), **Reset Scale to 100%** (Item 3), **Fit Screen** (Item 4), and **Collapse All/Expand All** (Item 5). 


<!-- PAGE_BREAK -->
 Workflow (Diagram View) | 126 

 Figure: The diagram view of the Workflow page 

 Table: State Elements In the Workflow Visual Editor, a box with a state contains the following elements. 

 Element Description 

 Arrow You click an arrow (see Item 6 in the screenshot above) to expand or collapse the list of actions or event handlers that trigger transitions for this state. 

 More button You click the More button (Item 7) to invoke a More menu with the following commands: 

- **Edit State** : Opens the **_State_** dialog box, which you can use to modify the state. 

- **Add Transition** : Opens the **_Add Transition_** dialog box, which you can use to add a     transition from the current state to another state. In the dialog box, you specify the     action or event handler that causes the transition, and the target state. 

- **Delete State** : Deletes the state. When you select this command, you need to con-     firm the deletion in the dialog box that is opened. 

 Plus button You click a plus button (Item 8) to manually draw a transition line for an action or an event handler that does not yet have any outgoing transitions from the current state. This opens the Add Transition Dialog Box dialog box with the Target State box filled in. 

 When the transition is created, the action or event handler that triggers it is added to the box with the current state with the name you have specified in the Trigger Name box of the dialog box. 

### Page Toolbar and the More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as 


<!-- PAGE_BREAK -->
 Workflow (Diagram View) | 127 

commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Command Description 

 Add Predefined State Opens the Add Predefined State dialog box, which you use to add a predefined state to the workflow. 

 Add State Opens the Add State dialog box, which you use to add a new state to the workflow. 

 Add Transition Opens the Add Transition dialog box, which you use to add a transition to the workflow. 

 This command is available only if you select a state in the States and Transitions pane. 

 Change Parent State Opens the Change Parent State dialog box, which you use to select the parent state for the current state. 

 This command is available only if you select a state in the States and Transitions pane. 

 Tree View Changes the view of the workflow from the diagram view to the tree view. (In the tree view, you can click the Diagram View button to return to this view.) 

 View Changes Opens the Changes dialog box, which you use to view the changes in the workflow. This button is available only if the workflow is inherited (that is, based on a predefined workflow). 

**_Table: New Action Dialog Box_** 

The **New Action** dialog box opens when you click **Create** in the **Add Transition** dialog box, as well as when you click **Create Action** on the table toolbar of the **Actions** tab of the **State** dialog box. 

 Element Description 

 The dialog box has the following elements. 

 Action Type Read-only. The type of the action, which indicates that the action changes the state of an entity as a part of a workflow. 

 Action Name Required. The internal name of the action, which will be displayed on the Actions page and in the Workflow Editor. 

 Display Name Required. The name of the action that will be displayed on the applicable Acumatica ERP form. 

 Dialog Box The dialog box that will be displayed when the action is clicked. For details, see Workflow Elements: General Information. 

 Category The category of the More menu in which the menu command associated with the action will be displayed. The default list of categories depends on the form. To manage the categories, you click the Manage Categories button on the page toolbar. 


<!-- PAGE_BREAK -->
 Workflow (Diagram View) | 128 

 Element Description 

 Add to Toolbar A check box that indicates (if selected) that the action will be displayed as a button on the form toolbar as well as under the selected category of the More menu if the action is available for a record based on its state. If the action is available but no category is specified, the action will be displayed on the form toolbar and under the Other category. 

 If the check box is cleared, the action will not be displayed on the form toolbar but will be displayed on the More menu. 

 The dialog box also contains the following buttons. 

 OK Closes the dialog box and creates the action. 

 Cancel Closes the dialog box without creating the action. 

### Add State Dialog Box 

 You use the Add State dialog box, which opens when you click Add State , to add a new state to the workflow. 

 Element Description 

 The dialog box contains the following elements. 

 Identifier A single-letter identifier of the state (for example, H for On Hold ). 

 Description The display name of the state (for example, On Hold ). 

 Parent State The parent state of the current state. 

 If you select a parent state, the state you are creating becomes a nested one for this parent state. If this parent state is not a composite state yet (that is, if it does not contain any nested states), the parent state becomes a composite state. 

 If you leave this box empty, the created state is added to the bottom of the list of states on the States and Transitions pane. 

 The dialog box has the following buttons. 

 OK Closes the dialog box and adds the state to the workflow. 

 Cancel Closes the dialog box without adding the state. 

### Change Parent State Dialog Box 

 You use the Change Parent State dialog box, which opens when you click Change Parent State , to select the parent state for the current state. 

 Element Description 

 The dialog box contains the following elements. 

 State Read-only. The name of the current state. 


<!-- PAGE_BREAK -->
 Workflow (Diagram View) | 129 

 Element Description 

 Parent State The parent state of the current state. 

 If this box is empty and you select a value in it, the current state becomes a nested one. If the box contains a value and you remove it, the current state becomes an ordinary state (that is, neither composite nor nested). If you modify the value in this box, the current nested state moves to another composite state. 

 The dialog box has the following buttons. 

 OK Closes the dialog box and changes the parent state. 

 Cancel Closes the dialog box without saving your changes to the parent state. 

### Add Predefined State Dialog Box 

 You use the Add Predefined State dialog box to add a predefined state to the workflow. This dialog box opens when you click Add Predefined State on the form. 

 Element Description 

 The dialog box contains the following elements. 

 State The name of the predefined state. 

 Parent State The parent state for the predefined state. 

 If you leave this box empty, the state is added to the bottom of the list of states on the States and Transitions pane. 

 The dialog box has the following buttons. 

 OK Closes the dialog box and adds the predefined state to the workflow. 

 Cancel Closes the dialog box without adding the predefined state. 

### Add Transition Dialog Box 

 You use the Add Transition dialog box, which opens when you click Add Transition , to add a transition to the workflow. 

 Element Description 

 The dialog box contains the following elements. 

 Original State Read-only. The name of the state from which the transition is being created. 

 Triggered by Action An option button that indicates that the transition is triggered by an action. 

 Triggered by Event Handler 

 An option button that indicates that the transition is triggered by an event handler. 


<!-- PAGE_BREAK -->
 Workflow (Diagram View) | 130 

 Element Description 

 Trigger Name The name of the action or event handler that triggers the transition. You can select a name from the drop-down list. Alternatively, you can click Create (right of the box) and add a new action. 

 Create A button that you click to open the New Action dialog box, so that you can specify the settings of the new action. 

 This button is available if you select the Triggered by Action option button. 

 Condition Optional. The condition that must be fulfilled for the transition to take place. 

 Target State The target state of the transition. 

 In the box, you can select a nested state, a composite state, @Next (the next state in the composite state), or @ParentNext (the next state of the parent state). 

 This box is filled in when you create a transition by clicking the plus button and manually drawing a transition line. 

 The dialog box also contains the following buttons. 

 OK Closes the dialog box and adds the transition to the workflow. 

 Cancel Closes the dialog box without adding the transition. 

### Changes Dialog Box 

 You use this dialog box to view the source code of the workflow; the changes to the currently selected element (state or transition) are highlighted in red. The dialog box also contains the following buttons. 

 Button Description 

 Revert Changes Returns the workflow to its predefined state. 

 Close Closes the dialog box. 

### State Dialog Box 

 This dialog box opens when you click the More button for a state and then click Edit State. The dialog box contains a Summary area and the following tabs: Fields , Actions , Handlers , Fields to Update on Entry , and Fields to Update on Exit. 

 Table: State Dialog Box: Summary Area The Summary area of the dialog box contains the following elements. 

 Element Description 

 Identifier A single-letter identifier of the state (for example, H for On Hold ). 

 Description The display name of the state (for example, On Hold ). 


<!-- PAGE_BREAK -->
 Workflow (Diagram View) | 131 

 Element Description 

 Active A check box that indicates (if selected) that the selected state is active. 

 Initial State of the Workflow 

 A check box that indicates (if selected) that this state is the initial state of the workflow. 

**_Table: State Dialog Box: Fields Tab_** 

The **Fields** tab of **State** dialog box contains a table with the fields that have properties that should be modified for the current state. (For details, see _Conditions and Transitions: General Information_ .) Also, for fields of the _Combo_ type, specific combo box values can be specified. The tab has the following elements. 

 Element Description 

 The table toolbar includes standard buttons and the following table-specific button. 

 Combo Box Values Opens the Combo Box Values dialog box, where you can specify the list of values that are displayed as combo boxes. 

 The table on the tab has the following columns. 

 Active A check box that indicates (if selected) that the field is active for the selected state. 

 Object Name The name of the DAC from which the field is selected. 

 Field Name The name of the field. 

 Disabled A check box that indicates (if selected) that the field is unavailable for the selected state. 

 Hidden A check box that indicates (if selected) that the field is hidden for the selected state. 

 Required A check box that indicates (if selected) that the field is required for the selected state. 

 Default Value The default value of the field. 

 You can specify default values of fields only for the initial state of a workflow. 

 Status Read-only. The status of the field. 

 The column can have one of the following values: 

- _Inherited_ : The field that has been added to the predefined workflow. 

- _New_ : The field that you have added to the workflow. 

**_Table: State Dialog Box: Fields to Update on Entry and Fields to Update on Exit Tabs_** 

On the **Fields to Update on Entry** and **Fields to Update on Exit** tabs of the **State** dialog box, you specify which fields should be updated when an entity on the form enters the current state and when the entity leaves this state, respectively. 


<!-- PAGE_BREAK -->
 Workflow (Diagram View) | 132 

Before a transition is performed, the system checks the following: 

- For the target state, the fields that should be updated when the entity enters the state 

- For the original state, the fields that should be updated when the entity leaves the state 

The tab has the following elements. 

 Element Description 

 The tables on the tabs contain the same columns, which are listed in the following table. 

 Active A check box that indicates (if selected) that the field should be updated after the transition. 

 Field Name The name of the field that should be updated. 

 From Schema A check box that indicates (if selected) that the field value from the database should be used. 

 New Value The new value for the field. 

 Status The status of the field to update. 

 The column can have one of the following values: 

- _Inherited_ : The field that has been added to the predefined workflow. 

- _New_ : The field that you have added to the workflow. 

**_Table: State Dialog Box: Actions Tab_** 

The **Actions** tab of the **State** dialog box contains the list of actions specified for the state (for details, see _Action Configuration: General Information_ ).The tab has the following elements. 

 Element Description 

 The table toolbar includes standard buttons and the following table-specific button. 

 Create Action Opens the New Action dialog box, where you can create an action for the current state. 

 The table of the tab has the following columns. 

 Active A check box that indicates (if selected) that the action is active for the selected state. 

 Action An action that is available for the selected state. 

 Duplicate on Toolbar A check box that indicates (if selected) that the action should be available on the page toolbar (as a button) as well as on the More menu. 

 Auto-Run Condition A condition that (if fulfilled) makes the system trigger the action automatically. 

 For a system action, the box is unavailable for editing. 

 The default value of the box is False , which indicates that the system does not trigger the action automatically. 


<!-- PAGE_BREAK -->
 Workflow (Diagram View) | 133 

 Element Description 

 Connotation An optional color notation that you can assign to the action to give users additional information about it. For example, you can use connotations to indicate to users which action in the entity processing workflow is the one most likely to be taken, given the state of the entity, which actions require special consideration, and which actions provide links to additional information, such as reports. 

 On the More menu, a connotation is displayed as a dot of the selected color (see the list below) right of the associated menu command. If the action is also displayed on the form toolbar, it is highlighted in the selected color. 

 You can select one of the following options (with the corresponding colors noted): 

- _Primary_ : The primary color of the site theme 

- _Secondary_ : The secondary color of the site theme 

- _Success_ : Green 

- _Danger_ : Red 

- _Warning_ : Yellow 

- _Info_ : Blue 

- _Light_ : Light gray 

- _Dark_ : Dark gray For an action on a form with a workflow, you can also specify a connotation in the **Action Properties** dialog box of the Actions page. In this case, this connota- tion is used for this action in all states of an entity in the workflow. If in a specific state, another connotation is specified for the action, the state-specific connota- tion takes precedence. 

 Connotations are also supported for forms without workflows, but the connotations for these forms can be modified only through code. For details, see Action Customization: Connotation for an Action. 

 Status A read-only box that indicates the status of the action. 

 The status of the action can be one of the following: 

- _Inherited_ : The system action. 

- _New_ : The action that you have created. 

- _Modified_ : The system action that you have modified. 

 Dialog Box The name of the dialog box that is displayed when a user clicks the action, if applicable; in this dialog box, the user should enter the needed values. 

**_Table: State Dialog Box: Handlers Tab_** 

The **Handlers** tab of the **State** dialog box displays the event handlers that are available for the current state (for details, see _Conditions and Transitions: General Information_ ). The tab has the following elements. 

 Element Description 

 The table has the following columns. 

 Active A check box that indicates (if selected) that the event handler is active for the selected state. 


<!-- PAGE_BREAK -->
 Workflow (Diagram View) | 134 

 Element Description 

 Handler An event handler that is available for the selected state. 

 Status A read-only box that indicates the status of the event handler. 

 The column can have one of the following values: Inherited or New. 

### Transition Elements 

 In the Workflow Visual Editor, if a transition has a condition (that is, if the transition is performed only when a particular condition is met for the entity), a diamond icon is displayed above the transition (see Item 1 in the following screenshot). 

 If an action with a transition contains an auto-run condition (that is, a condition for which the action is triggered automatically if the condition is met), a lightning rod icon is displayed above the transition (Item 2). 

 The transition lines are of the same color as the states they originate from, which makes it easier to distinguish between transitions. Also, each transition has a dot that indicates the direction of the transition and that is of the same color as the target state (Item 3). 

 Figure: Elements of the transitions 

 Table: Transition Context Menu The context menu of a transition, which is displayed when you click the transition, contains the following commands. 

 Command Description 

 Edit Transition Opens the Transition dialog box. 


<!-- PAGE_BREAK -->
 Workflow (Diagram View) | 135 

 Command Description 

 Delete Transition Deletes the selected transition. When you select this command, you need to confirm the deletion in the dialog box that is opened. 

### Transition Dialog Box 

 This dialog box opens when you click the transition and then click the Edit button in the context menu. 

 Element Description 

 The dialog box contains the following elements. 

 Original State Read-only. The name of the state from which the transition is being created. 

 Active A check box that indicates (if selected) that the transition is active for the selected action. 

 Triggered by Action An option button that indicates that the transition is triggered by an action. 

 Triggered by Event Handler 

 An option button that indicates that the transition is triggered by an event handler. 

 Trigger Name The name of the action or event handler that triggers the transition. 

 Condition Optional. The condition that must be fulfilled for the transition to take place. 

 Target State The target state of the transition. This box is filled in when you create a transition by clicking the plus button and manually drawing a transition line. 

 The dialog box also contains the Fields to Update After Transition table, which lists the fields that the system should update after the transition is performed. The table has the following columns. 

 Active A check box that indicates (if selected) that the field should be updated after the transition. 

 Field Name The name of the field that should be updated. 

 From Schema A check box that indicates (if selected) that the field value from the database should be used. 

 New Value The new value for the field. 

 Status The status of the field to update. 

 The dialog box also contains the following button. 

 OK Closes the dialog box and applies the selected options. 


<!-- PAGE_BREAK -->
 Workflow (Tree View) | 136 

## Workflow (Tree View) 

 Page ID: (AU201030) 

 For a customized or custom workflow for a particular screen (that is, a form in Acumatica ERP), you use the Workflow page to define states, transitions, and actions. The page has a tree view, described in this topic, and a diagram view (also referred to as the Workflow Visual Editor ), which is described in Workflow (Diagram View). 

 You open the Workflow page by clicking Default Workflow or the name of the customized or custom workflow under the screen ID (of the form for which you are adding or modifying workflows) in the navigation pane of the Customization Project Editor. You can also open the page by clicking the link in the Workflow Name column of the Workflows page. The name that appears on the page consists of the form ID, the form name in parentheses, and State Diagram: <Workflow Name> Workflow. (This name is also used for the tree view of the workflow.) 

 If a particular form has only one predefined workflow, the workflow name of the predefined workflow is Default workflow. If the form has multiple predefined workflows, different workflow names are assigned to each predefined workflow. 

### Page Toolbar and More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Command Description 

 Add Predefined State 

 Opens the Add Predefined State dialog box, which you use to add a predefined state to the workflow. 

 This command is not available for a predefined workflow 

 Add State Opens the Add State dialog box, which you use to add a new state to the workflow. 

 This command is not available for a predefined workflow 

 Add Transition Opens the Add Transition dialog box, which you use to add a transition to the workflow. 

 This command is available only if you select a state or one of the nodes under Transitions in the States and Transitions pane. 

 This command is not available for a predefined workflow 

 Change Parent State 

 Opens the Change Parent State dialog box, which you use to select the parent state for the current state. 

 This command is available only if you select a state in the States and Transitions pane. 

 This command is not available for a predefined workflow 

 Diagram View Changes the view of the workflow from the tree view to the diagram view. (In the diagram view, you can click the Tree View button to return to this view.) 

 This command is unavailable if the selected workflow has composite states. 


<!-- PAGE_BREAK -->
 Workflow (Tree View) | 137 

 Command Description 

 View Changes Opens the Changes dialog box, which you use to view the changes in the workflow. This command is available only if the workflow is inherited (that is, based on a predefined workflow). 

 This command is not available for a predefined workflow 

**_Table: Add State Dialog Box_** 

You use the **Add State** dialog box, which opens when you click **Add State** , to add a new state to the workflow. 

 Element Description 

 The dialog box contains the following elements. 

 Identifier A single-letter identifier of the state (for example, H for On Hold ). 

 Description The display name of the state (for example, On Hold ). 

 Parent State The parent state of the current state. 

 If you select a parent state, the state you are creating becomes a nested one for this parent state. If this parent state is not a composite state yet (that is, if it does not contain any nested states), the parent state becomes a composite state. 

 If you leave this box empty, the created state is added to the bottom of the list of states on the States and Transitions pane. 

 The dialog box has the following buttons. 

 OK Closes the dialog box and adds the state to the workflow. 

 Cancel Closes the dialog box without adding the state. 

**_Table: Change Parent State Dialog Box_** 

You use the **Change Parent State** dialog box, which opens when you click **Change Parent State** , to select the parent state for the current state. 

 Element Description 

 The dialog box has the following elements. 

 State Read-only. The name of the current state. 

 Parent State The parent state of the current state. 

 If this box is empty and you select a value in it, the current state becomes a nested one. If the box contains a value and you remove it, the current state becomes an ordinary state (that is, neither composite nor nested). If you modify the value in this box, the current nested state moves to another composite state. 

 The dialog box has the following buttons. 

 OK Closes the dialog box and changes the parent state. 


<!-- PAGE_BREAK -->
 Workflow (Tree View) | 138 

 Element Description 

 Cancel Closes the dialog box without saving your changes to the parent state. 

**_Table: Add Predefined State Dialog Box_** 

You use the **Add Predefined State** dialog box to add a predefined state to the workflow. This dialog box opens when you click **Add Predefined State** on the form. 

 Element Description 

 The dialog box has the following elements. 

 State The name of the predefined state. 

 Parent State The parent state for the predefined state. 

 If you leave this box empty, the state is added to the bottom of the list of states on the States and Transitions pane. 

 The dialog box has the following buttons. 

 OK Closes the dialog box and adds the predefined state to the workflow. 

 Cancel Closes the dialog box without adding the predefined state. 

**_Table: Add Transition Dialog Box_** 

You use the **Add Transition** dialog box, which opens when you click **Add Transition** , to add a transition to the workflow. 

 Element Description 

 The dialog box contains the following elements. 

 Original State Read-only. The name of the state from which the transition is being created. 

 Triggered by Action An option button that indicates that the transition is triggered by an action. 

 Triggered by Event Handler 

 An option button that indicates that the transition is triggered by an event handler. 

 Trigger Name The name of the action or event handler that triggers the transition. You can select a name from the drop-down list or click Create (right of the box) and add the action. 

 Create A button that you click to open the New Action dialog box, so that you can specify the settings of the new action. 

 This button is available if you select the Triggered by Action option button. 

 Condition Optional. The condition that must be fulfilled for the transition to take place. 

 Target State The target state of the transition. 

 In the box, you can select a nested state, a composite state, @Next (the next state in the composite state), or @ParentNext (the next state of the parent state). 


<!-- PAGE_BREAK -->
 Workflow (Tree View) | 139 

 Element Description 

 The dialog box also contains the following buttons. 

 OK Closes the dialog box and adds the transition to the workflow. 

 Cancel Closes the dialog box without adding the transition. 

**_Table: New Action Dialog Box_** 

The **New Action** dialog box opens when you click **Create** in the **Add Transition** dialog box, as well as when you click **Create Action** on the table toolbar of the **Actions** tab. 

 Property Description 

 The dialog box has the following elements. 

 Action Type Read-only. An option that indicates that the action changes the state of an entity as a part of a workflow. 

 Action Name Required. The internal name of the action, which will be displayed on the Actions page and in the Workflow Editor. 

 Display Name Required. The name of the action that will be displayed on the applicable Acumatica ERP form. 

 Dialog Box The dialog box that will be displayed when the action is clicked. 

 Category The category of the More menu in which the menu command associated with the action will be displayed. The default list of categories depends on the form. To manage the categories, you click the Manage Categories button on the page toolbar of the Actions page. 

 Add to Toolbar A check box that indicates (if selected) that the action will be displayed as a button on the form toolbar as well as under the selected category of the More menu if the action is available for a record based on its state. If the action is available but no category is specified, the action will be displayed on the form toolbar and under the Other category. 

 If the check box is cleared, the action will not be displayed on the form toolbar but will be displayed on the More menu. 

 The dialog box also contains the following buttons 

 OK Closes the dialog box and creates the action. 

 Cancel Closes the dialog box without creating the action. 

**_Table: Changes Dialog Box_** 

You use this dialog box to view the source code of the workflow; the changes to the currently selected element (state or transition) are highlighted in red. The dialog box also contains the following buttons. 

 Button Description 

 Revert Changes Returns the workflow to the predefined state. 


<!-- PAGE_BREAK -->
 Workflow (Tree View) | 140 

 Button Description 

 Close Closes the dialog box. 

### States and Transitions Pane 

 The States and Transitions pane contains the tree view of states and transitions defined for the workflow. On the pane, the transitions that lead from a state to another state are displayed in the Transitions node under the node with the name of this state. The pane contains the following buttons. 

 These buttons are not available for a predefined workflow. 

 Button Description 

 Delete Deletes the selected state or transition (the one you clicked before clicking this button). 

 Move Up Moves up the selected state or transition (the one you clicked before clicking this button). 

 Move Down Moves down the selected state or transition (the one you clicked before clicking this button). 

### State Properties Tab: Summary Area 

 The State Properties tab is displayed when you click a state on the States and Transitions pane. It consists of a Summary area and three tabs in the lower part of the State Properties tab: Fields , Fields to Update on Entry , and Fields to Update on Exit. 

 The Summary area of the tab contains the following elements. 

 Element Description 

 Identifier A single-letter identifier of the state (for example, H for On Hold ). 

 Description The display name of the state (for example, On Hold ). 


<!-- PAGE_BREAK -->
 Workflow (Tree View) | 141 

 Element Description 

 Skip Condition The condition that the system checks when an entity enters any nested state in a composite state. If the condition is fulfilled, the nested state is skipped. The box is displayed only for a nested state in a composite state. 

 If this condition is fulfilled, the system does the following for the selected nested state: 

1. Assigns the default values for the fields as specified on the **Fields** tab if the select-     ed state is the initial state of the workflow 

2. Does not check the fields that should be updated when the entity enters the state     and leaves it 

3. Does not check any of the workflow settings 

4. Moves the entity to the next state in the composite state 

 If the box is empty, the system uses the typical workflow for this state. That is, the transitions are triggered only by actions or event handlers, and the system does not check the skip condition again while the entity remains in this state. 

 Next State Read-only. The state to which an entity will move if the skip condition is fulfilled and the entity skips the current state. The box is displayed only if you have selected a nested state. 

 Active A check box that indicates (if selected) that the selected state is active. 

 Initial State of the Workflow 

 A check box that indicates (if selected) that this state is the initial state of the workflow. 

### State Properties Tab: Fields Tab 

 The Fields tab, located in the lower part of the State Properties tab, contains a table with the fields whose properties should be modified for the current state. (For details, see Workflow Elements: General Information .) Also, for fields of the Combo type, specific combo box values can be specified. 

 Table: Table Toolbar The table toolbar includes standard buttons and the following table-specific button. 

 Button Description 

 Combo Box Values Opens the Combo Box Values dialog box, where you can specify the list of values that are displayed as combo boxes. 

 Table: Table Columns The tab includes the following columns. 

 Column Description 

 Active A check box that indicates (if selected) that the field is active for the selected state. 

 Object Name The name of the DAC from which the field is selected. 

 Field Name The name of the field. 


<!-- PAGE_BREAK -->
 Workflow (Tree View) | 142 

 Column Description 

 Disabled A check box that indicates (if selected) that the field is unavailable for the selected state. 

 Hidden A check box that indicates (if selected) that the field is hidden for the selected state. 

 Required A check box that indicates (if selected) that the field is required for the selected state. 

 Default Value The default value of the field. 

 You can specify default values of fields only for the initial state of a workflow. 

 Status Read-only. The status of the field. 

 The column can have one of the following values: Inherited or New. 

### State Properties Tab: Fields to Update on Entry and Fields to Update on Exit Tabs 

 On the Fields to Update on Entry and Fields to Update on Exit tabs, you specify which fields should be updated when an entity on the form enters the current state and when the entity leaves this state, respectively. These tabs are located in the lower part of the State Properties tab. 

 Before a transition is performed, the system checks the following: 

- For the target state, the fields that should be updated when the entity enters the state 

- For the original state, the fields that should be updated when the entity leaves the state 

 Table: Table Columns The tables on the tabs contain the same columns, which are described below. 

 Column Description 

 Active A check box that indicates (if selected) that the field should be updated after the transition. 

 Field Name The name of the field that should be updated. 

 From Schema A check box that indicates (if selected) that the field value from the database should be used. 

 New Value The new value for the field. 

 Status The status of the field to update. 

 The column can have one of the following values: 

- _Inherited_ : The field that has been added to the predefined workflow. 

- _New_ : The field that you have added to the workflow. 


<!-- PAGE_BREAK -->
 Workflow (Tree View) | 143 

### Actions Tab 

 The Actions tab is displayed when you click a state on the States and Transitions pane. The Actions tab contains the list of actions specified for the state (for details, see Action Configuration: General Information ). 

 Table: Table Toolbar The table toolbar includes standard buttons and the following table-specific button. 

 Button Description 

 Create Action Opens the New Action dialog box, where you can create an action for the current state. 

 Table: Table Columns The table has the following columns. 

 Column Description 

 Active A check box that indicates (if selected) that the action is active for the selected state. 

 Action An action that is available for the selected state. 

 Duplicate on Toolbar A check box that indicates (if selected) that the action should be available on the page toolbar (as a button) as well as on the More menu. 

 Auto-Run Allowed A read-only check box that indicates (if selected) that the action can be triggered automatically. 

 If this check box is selected for an action, to trigger this action automatically, you need to specify the condition in the Auto-Run Condition column. 

 Predefined system actions cannot be triggered automatically. 

 Auto-Run Condition A condition that (if fulfilled) makes the system trigger the action automatically. 

 This box is unavailable for editing if the Auto-Run Allowed check box is cleared for the action. 

 If the Auto-Run Allowed check box is selected for the action, the default value of this box is False , which indicates that the system does not trigger the action automatically. 


<!-- PAGE_BREAK -->
 Workflow (Tree View) | 144 

 Column Description 

 Connotation An optional color notation that you can assign to the action to give users additional information about it. For example, you can use connotations to indicate to users which action in the entity processing workflow is the one most likely to be taken, given the state of the entity, which actions require special consideration, and which actions provide links to additional information, such as reports. 

 On the More menu, a connotation is displayed as a dot of the selected color (see the list below) to the right of the associated menu command. If the action is also displayed on the form toolbar, it is highlighted in the selected color. 

 You can select one of the following options (with the corresponding colors noted): 

- _Primary_ : The primary color of the site theme 

- _Secondary_ : The secondary color of the site theme 

- _Success_ : Green 

- _Danger_ : Red 

- _Warning_ : Yellow 

- _Info_ : Blue 

- _Light_ : Light gray 

- _Dark_ : Dark gray For an action on a form with a workflow, you can also specify a connotation in the **Action Properties** dialog box of the Actions page. In this case, this connotation is used for this action in all states of an entity in the workflow. If in a specific state, an- other connotation is specified for the action, the state-specific connotation takes precedence. 

 Connotations are also supported for forms without workflows, but the connotations for these forms can be modified only through code. For details, see Action Customization: Connotation for an Action. 

 Status A read-only box that indicates the status of the action. 

 The status of the action can be one of the following: 

- _Inherited_ : The system action. 

- _New_ : The action that you have created. 

 Dialog Box The name of the dialog box that is displayed when a user clicks the action, if applicable; in this dialog box, the user should enter the needed values. 

### Handlers Tab 

 The Handlers tab is displayed when you click a state on the States and Transitions pane. The Handlers tab displays the event handlers that are available for the current state (for details, see Conditions and Transitions: General Information ). The columns of the table are described below. 

 The table toolbar includes only standard buttons. For the list of standard buttons, see Table Toolbar. 


<!-- PAGE_BREAK -->
 Workflow (Tree View) | 145 

 Column Description 

 Active A check box that indicates (if selected) that the event handler is active for the selected state. 

 Handler An event handler that is available for the selected state. 

 Status A read-only box that indicates the status of the event handler. 

 The column can have one of the following values: Inherited or New. 

### Transition Properties Tab 

 The Transition Properties tab is displayed when you click a transition on the States and Transitions pane. 

 The tab includes the following elements and the Fields to Update Aer Transition table. 

 Table: Transition Properties Elements You can use the following elements to define the transition. 

 Element Description 

 Original State Read-only. The name of the state from which the transition is performed. 

 Active A check box that indicates (if selected) that the transition is active. 

 Triggered by Action An option button that indicates that the transition is triggered by an action. 

 Triggered by Event Handler 

 An option button that indicates that the transition is triggered by an event handler. 

 Trigger Name The name of the action or event handler that triggers the transition. 

 Condition Optional. The condition that should be fulfilled for the transition to take place. 

 Target State The target state of the transition. 

 Table: Fields to Update Aer Transition Table The Fields to Update Aer Transition table lists the fields that the system should update aer the transition is performed, and contains the following columns. 

 Column Description 

 Active A check box that indicates (if selected) that the field should be updated after the transition. 

 Field Name The name of the field that should be updated. 

 From Schema A check box that indicates (if selected) that the field value from the database should be used. 

 New Value The new value for the field. 


<!-- PAGE_BREAK -->
 Workflow (Tree View) | 146 

**Column Description** 

**Status** The status of the field update. 


<!-- PAGE_BREAK -->
 Workflows | 147 

## Workflows 

 Page ID: (AU201020) 

 This page contains the list of all workflows defined for a particular screen (that is, a form in Acumatica ERP) as well as the general settings of each workflow. The page lists predefined workflows, as well as customized and custom workflows. You can use the page to add customized and custom workflows for the form. 

 You open the Workflows page by clicking Workflows under the screen ID (of the form for which you are adding or modifying workflows) in the navigation pane of the Customization Project Editor. In the name that appears on the page, Workflows is preceded by the form ID and then the form name in parentheses. 

### Page Toolbar and More Menu 

 The page toolbar includes standard buttons and page-specific buttons and commands. For the list of standard buttons, see Page Toolbar. The page-specific commands can be shown as buttons on the page toolbar, as commands on the More menu, or in both places. These commands are listed in the following table in alphabetical order. 

 Command Description 

 Add Workflow Opens the Add Workflow dialog box, which you use to add a new custom workflow or a new inherited workflow—that is, a workflow based on a predefined workflow. 

 Disinherit Breaks the relationship between the predefined workflow and the selected customized workflow that was based on it. (You first click the row with the customized workflow in the table and then click this command.) The selected workflow will no longer get updates from the system, and the Upgrade Predefined Workflow command will not be available for it. 

 You cannot reverse the changes induced by the Disinherit command. That is, you cannot link the selected workflow to a predefined workflow once you have selected the workflow and clicked Disinherit. 

 Upgrade Predefined Workflow 

 Starts the process of upgrading the selected customized workflow (which is based on a predefined workflow) with the latest changes from the system. (You first click the row with the customized workflow in the table and then click this command.) 

 If there are any conflicts, the Upgrade Conflicts dialog box opens, in which you can resolve these conflicts. 

 This command is available only if the version of the predefined workflow in the system and the version of the predefined workflow in the customization project differ. 

 View Changes Opens the Changes dialog box, which you use to view the description of a workflow in internal format. If you have made changes to this workflow, they are highlighted in the dialog box. You can return the workflow to the predefined state by clicking Revert Changes in the dialog box. 

 The View Changes button and command are available only if the workflow is inherited—that is, based on a predefined workflow. 


<!-- PAGE_BREAK -->
 Workflows | 148 

**_Table: Add Workflow Dialog Box_** 

This dialog box opens when you click **Add Workflow** on the page toolbar. The dialog box contains the following elements. 

 Element Description 

 Operation The operation that the system will perform when you specify all the needed values and click OK. You can select one of the following options: Create New Workflow , Extend System Workflow , and Copy Workflow. 

 You can select one of the following options: 

- _Create New Workflow_ : Creates custom workflow 

- _Extend System Workflow_ : Creates a customized workflow 

- _Copy Workflow_ : Creates a copy of a predefined workflow 

 Base Workflow Required. The name of the predefined workflow on which the current workflow is based. 

 This box is displayed only if you select Extend System Workflow in the Operation box. 

 Workflow to Copy Required. The predefined workflow that you want to copy. 

 This box is displayed only if you select Copy Workflow in the Operation box. 

 Workflow Type Required. The type of the entities to which the workflow is applied. The applicable entities depends on the particular form for which the workflow is defined. 

 If only one default workflow is available for the form, this box contains one value ( Default ). If the form has multiple workflows, this box contains all of these workflow types, and the Default type. 

 Workflow Name Required. The name of the workflow you are adding. 

 This dialog box has the following buttons. 

 OK Adds the workflow to the table on the page and closes the dialog box. 

 Cancel Closes the dialog box without adding a workflow to the page. 

**_Table: Upgrade Conflicts Dialog Box_** 

This dialog box opens when you click **Upgrade Predefined Workflow** on the page toolbar. The dialog box contains the following elements. 

 Element Description 

 Workflow Element The workflow element in which the conflict has occurred. 

 Property The property of the workflow element in which the conflict has occurred. 

 System Value The value that the element has in the system workflow, 

 Customization Value The value that the element has in the customized workflow. 

 System Action The action that the system has performed to modify the element. 


<!-- PAGE_BREAK -->
 Workflows | 149 

 Element Description 

 Customization Action The customization action that has been performed to modify the element. 

 Resolve Conflict in Action The action that the system will perform to resolve the conflict. 

 This dialog box has the following buttons. 

 OK Resolves the conflicts, merges the changes, and closes the dialog box. 

 Cancel Closes the dialog box without resolving the conflicts. 

 Table: Changes Dialog Box You use this dialog box to view the source code of the workflow; the changes to the currently selected element are highlighted in red. The dialog box also contains the following buttons. 

 Button Description 

 Revert Changes Returns the workflow to the predefined state. 

 Close Closes the dialog box. 

### Summary Area 

 In this area, you can specify the basic settings for the new workflow. 

 Element Description 

 State Identifier The name of the field on this form that indicates the state. 

 Type Identifier The field whose value determines which workflow is used if multiple workflows are defined for the form. 

 If you do not select any value in the this box, an entity that has been created on the form can have only one workflow. If you want the entity to have multiple workflows, select the field that defines the change of the workflow in this box. 

 This field is read-only if its value has been specified in the code (by using Workflow API). 

 Allow Users to Modify Type A check box that you select if you want users to be able to change the workflow type for an existing entity. 


<!-- PAGE_BREAK -->
 Workflows | 150 

 Element Description 

 Subtype Identifier The field whose value determines which workflow is used if multiple workflows are defined for the form (that is, the workflow-identifying field of the second level). 

 This box is available only if the type identifier for this workflow is specified in the code (by using Workflow API). By default, it is supported for the following forms: 

- _Sales Orders_ (SO30100) 

- _Purchase Orders_ (PO301000) 

- _Purchase Receipts_ (PO302000) 

- _Landed Costs_ (PO303000) 

- _Subcontracts_ (SC301000) 

- _Service Orders_ (FS300100) 

- _Appointments_ (FS300200) 

 Allow Users to Modify Subtype 

 A check box that you select if you want users to be able to change the workflow subtype for an existing entity. 

### Table 

 This table lists all workflows defined for the form. If you click the name of a workflow in the table, you open the Workflow page with the workflow. This page has the name <Form Number (Form Name)> State Diagram: <Workflow Name> for the customized, custom, or predefined workflow. The columns of the table are described below. 

 The table toolbar includes only standard buttons. For the list of standard buttons, see Table Toolbar. 

 Column Description 

 Active A check box that indicates (if selected) that the current workflow is active. 

 Workflow Type The type of the entities to which the workflow is applied. The applicable entities depends on the particular form for which the workflow is defined. 

 Workflow Subtype The subtype of the entities to which the workflow is applied. 

 This box is available only if the type identifier for this workflow is specified in the code (by using Workflow API). 

 Workflow Name The name of the workflow, which is also a link that you can click to switch to the Workflow page for the selected workflow. 

 Base System Workflow 

 The name of the predefined workflow on which the current workflow is based. 

 Status The status of the workflow, which can be one of the following: System Read-Only , Inherited , or New. 


