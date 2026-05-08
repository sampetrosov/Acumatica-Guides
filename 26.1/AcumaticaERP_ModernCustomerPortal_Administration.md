## Administrator Guide 

# Modern Customer Portal 

# Administrator Guide 

# 2026 R1 


<!-- PAGE_BREAK -->
 Contents | 2 

## Contents 

 Copyright...............................................................................................................................................3 

 Modern Customer Portal Administration: General Information...................................................................4 

 Creating a Portal.................................................................................................................................... 7 

 Modern Customer Portal: Portal Deployment..................................................................................................7 

 Modern Customer Portal: Completing Portal Setup........................................................................................ 9 

 Modern Customer Portal: Catalog Configuration.......................................................................................... 13 

 Assigning Roles to Portal Users..............................................................................................................21 

 Modern Customer Portal: Access Rights Through Predefined Roles.............................................................21 

 Modern Customer Portal: Role Assignment in Acumatica ERP..................................................................... 23 


<!-- PAGE_BREAK -->
 Copyright | 3 

## Copyright 

**©** (^) **2026 Acumatica, Inc. ALL RIGHTS RESERVED.** No part of this document may be reproduced, copied, or transmitted without the express prior consent of Acumatica, Inc. 3075 112th Avenue NE, Suite 200, Bellevue, WA 98004, USA 

#### Restricted Rights 

 The product is provided with restricted rights. Use, duplication, or disclosure by the United States Government is subject to restrictions as set forth in the applicable License and Services Agreement and in subparagraph (c)(1)(ii) of the Rights in Technical Data and Computer Soware clause at DFARS 252.227-7013 or subparagraphs (c)(1) and (c)(2) of the Commercial Computer Soware-Restricted Rights at 48 CFR 52.227-19, as applicable. 

#### Disclaimer 

 Acumatica, Inc. makes no representations or warranties with respect to the contents or use of this document, and specifically disclaims any express or implied warranties of merchantability or fitness for any particular purpose. Further, Acumatica, Inc. reserves the right to revise this document and make changes in its content at any time, without obligation to notify any person or entity of such revisions or changes. 

#### Trademarks 

 Acumatica is a registered trademark of Acumatica, Inc. HubSpot is a registered trademark of HubSpot, Inc. Microso Exchange and Microso Exchange Server are registered trademarks of Microso Corporation. All other product names and services herein are trademarks or service marks of their respective companies. 

 Soware Version: 2026 R1 

 Last Updated: 03/30/2026 


<!-- PAGE_BREAK -->
 Modern Customer Portal Administration: General Information | 4 

## Modern Customer Portal Administration: General 

## Information 

 The Modern Customer Portal is a customer-facing site connected to your Acumatica ERP system. Each portal allows a customer’s employees to interact with your company online, based on how you configure the portal and specify portal users’ access rights. 

 The Modern Customer Portal and Acumatica ERP use the same records. Allowable changes made in one place to a record—for example, a contact’s job title or a company’s email address—are immediately reflected in the other place. 

 In this guide, portal users refers to employees of your customer who use the Modern Customer Portal. 

 The portal owner refers to a company that runs Acumatica ERP and creates, configures, and manages portals for its external users. 

 The support team refers to the team of the portal owner that processes cases submitted by portal users. These users submit cases in the portal and support team members review and manage these cases in Acumatica ERP. 

 This topic explains the key concepts behind portal administration. 

#### Applicable Scenarios 

 A customer company buys products repeatedly and wants to use a convenient customer portal connected to the portal owner’s ERP system to interact quickly: place orders, make payments, or check financial data. If portal users need to communicate with the support team, they can submit cases and obtain related information through the portal. 

 A portal owner wants to provide customers with online access to orders, invoices, payments, and support cases instead of handling these requests by email or phone. 

 An administrator of the portal owner needs to create and configure a portal in Acumatica ERP, create portal users, and assign roles to them. If needed, the administrator configures the Catalog (SP504001) form to specify the default items that are visible to portal users. 

#### Portal Architecture 

 A customer portal in the Modern Customer Portal consists of: 

- A portal instance deployed through the Acumatica ERP Configuration wizard and connected to your     Acumatica ERP database. This instance provides the website framework. 

- A record representing each portal, which you create on the _Portals_ (SP701000) form. This record defines how     the portal behaves—what functionality is available, what settings apply, and which users can access it. You manage all portals centrally in Acumatica ERP. 

#### System Features and Portal Forms 

 Some portal capabilities require system features to be enabled on the Enable/Disable Features (CS100000) form of Acumatica ERP: 

- _Modern Customer Portal_ (required) 

- _Inventory and Order Management_ 

- _Case Management_ 


<!-- PAGE_BREAK -->
 Modern Customer Portal Administration: General Information | 5 

 These features are enabled or disabled system-wide. Then for each portal, you select the categories whose forms should be made available, as well as the individual forms to be available in the portal. 

 This structure allows you to control access at a granular level. 

#### Managing Portals in Acumatica ERP 

 With the Portals (SP701000) form of Modern Customer Portal, you can brand and manage all portals for different customer accounts. On this form, you can: 

- **Manage multiple portals in one place:** You can view all portal instances and update their settings without     leaving Acumatica ERP. 

- **Apply consistent settings:** You can easily maintain consistent settings as needed—when you're creating     portals for customers who purchase similar items and may have common settings, such as case class,     visible warehouses, and processing center. You can also apply branding options consistently. 

- **Tailor each portal's settings:** You can enter customer-specific information and change the settings to     reflect the way this customer works with your company. This flexibility can be useful, for example, if you're     creating portals whose warehouses, branding, and CRM settings depend on the branch of your company     they work with. 

#### Roles and Access Control 

 You can control access to portal functionality through predefined roles—which define which forms and actions are available to portal users. Each portal user must be assigned at least one role. Roles can be assigned: 

- In Acumatica ERP by you or another administrator 

- In the portal by an authorized portal manager 

#### Portal Administration 

 You do the following to configure a customer portal: 

1. Deploy a portal instance. 

2. Create and configure the portal on the _Portals_ (SP701000) form. 

3. Select the available categories and forms available in the portal. 

4. Specify finance, ordering, CRM, payment, and branding settings. 

5. Assign roles to portal users. 

 Once you’ve created portals for customers, you can use the Portals (SP7010PL) list of records, shown below, as a starting point for working with any portal. From here, you can add a portal or view and edit any portal's configuration on the Portals form. 


<!-- PAGE_BREAK -->
 Modern Customer Portal Administration: General Information | 6 

**_Figure: All portals in Acumatica ERP_** 


<!-- PAGE_BREAK -->
 Creating a Portal | 7 

## Creating a Portal 

 In the Modern Customer Portal, your customers can view information about their interactions with you and perform common tasks online. As an Acumatica ERP administrator, you can quickly create each customer portal, manage its settings, and set up its catalog. 

 In this chapter, you’ll learn how to: 

- Create and configure a customer portal in Acumatica ERP 

- Manage portal settings 

- Perform system-wide configuration of the Catalog (SP504001) form in the Modern Customer Portal to     control which details appear for each catalog item 

### Modern Customer Portal: Portal Deployment 

 This topic explains how to deploy a new portal instance and create a portal in the Acumatica ERP Configuration wizard so that it’s ready for further configuration. 

 At a glance: Portal deployment 

1. Deploy a portal instance by using the Acumatica ERP Configuration wizard. 

2. Update the Web.config file. 

3. Create the portal on the Portals (SP701000) form of Acumatica ERP. 

 Who performs these steps: An Acumatica ERP administrator of the portal owner—the company whose customers will use the Modern Customer Portal. 

 The sections that follow describe these steps in detail. 

#### Creating a Portal Instance in Acumatica ERP 

 To begin, you use the Acumatica ERP Configuration wizard to deploy a new portal instance—just as you would when creating an Acumatica ERP instance. Do the following: 

1. On the Welcome page, click **Deploy a New Acumatica ERP Instance**. 

2. On the Database Server Connection page, specify the database server type and name, as well as the     authentication method. 

3. On the Database Configuration page, select **Connect to an Existing Database** and select the Acumatica ERP     database the portal instance will be connected to. 

 When a portal is linked to the Acumatica ERP database, it displays customer-related data, including available items, orders, invoices, payments, support cases, and financial information. 

4. On the Database Connection page, specify the sign-in credentials that Acumatica ERP will use to connect to     the database. 

5. On the Instance Configuration page, enter the portal instance’s name and make sure that the **Create**     **Modern Portal** option button is selected. 

6. On the Website Configuration page, specify the website and application pool settings.     Make sure that the **Use Modern UI as Default** check box is selected. Portal forms are available only in the     Modern UI. 


<!-- PAGE_BREAK -->
 Creating a Portal | 8 

7. On the RabbitMQ Configuration page, make sure that the **Set up RabbitMQ Configuration on this server**     **automatically** option button is selected. 

8. On the Confirmation of Configuration page, review your settings and click **Finish**. 

 The system creates a new Acumatica ERP instance, which you’ll use as a portal instance. 

#### Editing the Web.config File 

 When installing the portal, you must also configure additional parameters in a Web.config file to ensure that both applications work correctly with the same database. 

 Do the following: 

- **In a non-cluster environment** , set the IsMultiSiteMode parameter to True in the Web.config files     of Acumatica ERP and the Modern Customer Portal. 

 IsMultiSiteMode="true" 

- **In a cluster environment** , set the IsClusterEnabled parameter to True in the Web.config file of     Acumatica ERP. 

 IsClusterEnabled="true" 

#### Creating the Customer Portal in Acumatica ERP 

 Next, you open the Portals (SP701000) form in Acumatica ERP and start creating the portal. 

 Make sure the Modern Customer Portal feature is enabled on the Enable/Disable Features (CS100000) form. 

 Do the following in the Summary area of the form (see below): 

1. Enter a portal name and description. 

2. Enter the full portal URL (for example, _https://yourserver/CompanyPortal_ ). 

3. Select _Customer Portal_ in the **Portal Type** box. 


<!-- PAGE_BREAK -->
 Creating a Portal | 9 

 Figure: The new portal's basic settings 

#### What's Next? 

 Before saving the portal , you must specify its settings on the tabs of the Portals (SP701000) form. See the next topic, Modern Customer Portal: Completing Portal Setup , to learn how to complete the portal creation process. 

### Modern Customer Portal: Completing Portal Setup 

 You complete the portal creation process by specifying additional settings on the tabs of the Portals (SP701000) form. 

 You must enter all required settings before you can save the new portal. Portal users with the appropriate access rights can then sign in to the portal and use it. 

 At a Glance: Portal Setup Completion 

1. Select the categories and forms that will be available in the portal 

2. Specify finance, order, and customer relationship management (CRM) settings 

3. Save the portal to make it available 

4. Specify branding and landing page settings 

 Who performs these steps: An Acumatica ERP administrator of the portal owner—the company whose customers will use the Modern Customer Portal. 


<!-- PAGE_BREAK -->
 Creating a Portal | 10 

 The sections that follow describe these steps. 

#### Controlling the Available Forms 

 On the General tab of the Portals (SP701000) form, you specify which categories and forms are available in the portal. The tab shows a navigation pane (Item 1 below) with check boxes for: 

- **Categories (top-level nodes):** Select a category’s check box to make its forms available. If a category’s     check box is cleared, the check boxes for its forms are also cleared and unavailable for editing. 

- **Forms within categories:** Select a form’s check box to make the form available to portal users. If a form’s     check box is cleared, the form is hidden from portal navigation and can’t be opened, even when its URL is     entered directly. 

 Figure: Check boxes for categories and forms 

 In the Others section (Item 2), you can select uncategorized forms to make them available in the portal. These might include dashboards, generic inquiry forms, and pivot tables that you create in Acumatica ERP and then add to the portal. 

 If you haven't added uncategorized forms, the Others section is hidden, and you'll see a warning about the steps you need to take to secure these forms' data. 


<!-- PAGE_BREAK -->
 Creating a Portal | 11 

#### Security Requirements for Forms Your Company Creates 

 In Acumatica ERP, sensitive customer-related data includes data associated with a customer’s business account, such as cases, orders, invoices, payments, and debit and credit memos. This data needs to be protected on all forms, including dashboards, generic inquiry forms, pivot tables, custom and customized forms. 

 When you create custom or customized forms for use in the Modern Customer Portal (which appear in the Others section of the General tab), follow these guidelines: 

- Limit your company’s data that’s visible to portal users. 

- Ensure that each customer’s data is visible only to that customer’s portal users. 

 Predefined portal forms already meet these security requirements. For forms that you create or customize in Acumatica ERP for use in the portal, review the filters, visible UI elements, and row-level security settings to ensure that portal users can access only the data allowed by their assigned roles. 

 You can use the following filtering approaches: 

- BAccount-based filtering: Compare the BAccount record of the new form to the BAccount record of the     existing form in the system. You can use built-in portal filters, including filtering by the current BAccount     and its child BAccounts tree. 

- Visibility-based filtering: Select only records visible to the current user by using the CurrentMatch     condition. You can use the following conditions to validate data: 

- Restriction.PortalCustomers. This filter is equivalent to PXAccess.GetBAccountIDTree()     filtering. It selects only data related to the current BAccount and its child BAccounts. 

 SelectFrom<SPCRCase>.Where<SPCRCase.customerID.IsInSequence <Restriction.PortalCustomers>> 

- Restriction.PortalConsolidatedCustomers. This filter selects data for the current account’s     consolidating family. 

 SelectFrom<SPSOOrder>. Where<SPSOOrder.customerID.IsInSequence<Restriction.PortalConsolidatedCustomers>> 

- CurrentMatch. This filter selects data that’s visible to the signed-in user. 

 SelectFrom<InventoryItem>.Where<CurrentMatch<InventoryItem, AccessInfo. userName>> 

 When you create a customized generic inquiry form, on the Conditions tab of the Generic Inquiry (SM208000) form ( Value 1 column), filter data by using the following conditions: 

- Current BAccount: @mybaccount filter variable 

- Current BAccount tree: @mybaccounttree (current BAccount and all descendant BAccounts) Alternatively, you can filter data by the signed-in user or current contact. 

#### Specifying Finance, Order, and CRM Settings 

 On the Portals (SP701000) form, you can specify settings that will be used by portal forms. These include: 

- In the **Portal Access Role** box (Item 1 below), select the role assigned to portal users. For external     customers, select _Portal Users_. 


<!-- PAGE_BREAK -->
 Creating a Portal | 12 

- In the **User Type** box (Item 2), specify the user type of users who can access the portal. For external     customers, specify _Portal External User_. 

- In the **Finance and Order Management** section (Item 3), specify the financial source (the company or     branch the portal obtains data from), the default warehouse and sales order type for portal orders, and     warehouse visibility settings. 

- In the **CRM and Support** section (Item 4), select the default case class for cases submitted in the portal and     the default contact class for contacts created in the portal. 

- In the **Payments** section (Item 5), enter the customer’s default payment processing center and payment     methods. 

- In the **Address Lookup Plug-In** section (Item 6), you can specify a plug-in to support address lookup and     validation. 

 Figure: The general portal settings 

 When you enter the required portal settings, you can save the form. This action completes the portal creation process. Now portal users with appropriate rights can sign in to the portal and start working in it. 

 At this stage, you won’t use the Portal Users tab; defining portal users is a separate process described in Modern Customer Portal: Role Assignment in Acumatica ERP. 

#### Specifying Display and Landing Page Settings 

 On the Portal Settings tab of the Portals (SP701000) form, you can specify the display and landing page settings: 

- In the **Display Settings** section (Item 1 below), specify the interface theme, primary color, and company     name. You can also upload the company logo and sign-in image to reinforce branding. 

- In the **Landing Page Settings** section (Item 2), specify the default Home form and enter the text to be shown     at the top of the screen and on the **Go to Catalog** button. You can also upload images for the top message     and the **Go to Catalog** button. 


<!-- PAGE_BREAK -->
 Creating a Portal | 13 

 You can also control the visibility of navigation panels, the top message, and the Go to Catalog button by using the Display Navigation Panels , Display Top Message , and Display Go to Catalog Button check boxes (Items 3—4). 

 Figure: Branding and landing page settings 

 Save your changes again. 

#### What's Next? 

 Aer you’ve set up a portal, you need to assign roles to portal users. For more information, see Assigning Roles to Portal Users. 

### Modern Customer Portal: Catalog Configuration 

 You can tailor the Catalog (SP504001) form in the Modern Customer Portal to control which item details are visible —without customization or coding. 

 This topic explains how to perform this system-wide form configuration so that portal users see only the information you want them to see for items. 

 At a Glance: Configuration of the Catalog Form 

1. Activate UI Configuration mode on the Catalog form. 

2. For catalog item you want to modify:     a. Turn on UI Configuration mode.     b. Activate UI Configuration mode for the **Item Details** dialog box.     c. Add or remove elements in the dialog box. 


<!-- PAGE_BREAK -->
 Creating a Portal | 14 

 If you modify at least one item on the Catalog form, the changes apply to all items on the form. 

3. Apply the changes to all items. 

 Who performs these steps: An Acumatica ERP administrator of the company whose customers will use the Modern Customer Portal. Below you'll find the start-to-finish details about performing this process. 

#### System-Wide Form Configuration 

 In the Modern UI of Acumatica ERP, an administrator can configure the layout of any form and share that layout with all system users. 

 In the Modern Customer Portal, this system-wide form configuration is available only on the Catalog (SP504001) form. 

 This limitation applies to Acumatica ERP 2026 R1 only. 

 On this form, you control which item details are visible to portal users by default—so they see only the information you’ve chosen to display. 

 Other portal forms don’t support system-wide UI configuration. Administrators aren’t linked to specific customer accounts and thus can’t view or configure customer-specific data, such as order details, financial documents, and cases. 

#### UI Configuration Mode on the Catalog Form 

 To begin, on the Catalog (SP504001) form, click the Settings button (Item 1 below) on the form title bar and then click UI Configuration (Item 2). 


<!-- PAGE_BREAK -->
 Creating a Portal | 15 

 Figure: Activating UI Configuration mode on the Catalog form 

 UI Configuration mode is now active (Item 1 below) for the Catalog form. 

#### UI Configuration Mode for an Item 

 To switch on this mode for a specific catalog item, do the following: 

1. Click the Settings button in the upper right corner of that item (Item 2) 

 Figure: Using UI Configuration mode 


<!-- PAGE_BREAK -->
 Creating a Portal | 16 

2. Click the UI configuration button in the **Item Details** dialog box, which opens (Item 1 below) 

3. Click **UI Configuration** (Item 2) 

 Figure: Activating UI Configuration mode for the Item Details dialog box 

UI Configuration mode is now active for the **Item Details** dialog box for the item. 


<!-- PAGE_BREAK -->
 Creating a Portal | 17 

 Figure: Preparing to configure the item's visible details 

#### UI Configuration Mode for the Item Details Dialog Box 

 While UI Configuration mode is active for the Item Details dialog box, click the Settings button. 


<!-- PAGE_BREAK -->
 Creating a Portal | 18 

**_Figure: Configuring the item's details_** 

The system opens the **Section Configuration** dialog box. Here you can add or remove selected elements from the **Item Details** dialog box. When you complete the configuration, all portal users will see the selected elements for each item. 


<!-- PAGE_BREAK -->
 Creating a Portal | 19 

**_Figure: Selecting elements to be shown for each item_** 

To finish the configuration, do the following: 

1. Click **Apply** and then **Overwrite Personal Configuration** (Item 1) 

2. Click **Apply to All** 


<!-- PAGE_BREAK -->
 Creating a Portal | 20 

 Figure: Completing the configuration 

Applying the changes to all ensures that the selected layout is used for every item on the Catalog (SP504001) form. 


<!-- PAGE_BREAK -->
 Assigning Roles to Portal Users | 21 

## Assigning Roles to Portal Users 

 Roles determine which forms and actions are available to each portal user in the Modern Customer Portal. Each role includes a defined set of access rights, and every portal user must have at least one role assigned. Roles can be assigned by: 

- An Acumatica ERP administrator 

- An authorized portal user directly in the Modern Customer Portal When you create a portal contact—a record representing a customer’s employee who will use the portal—the contact becomes visible in both Acumatica ERP and the Modern Customer Portal. Aer you select a user type and assign one or more roles to the contact, the system creates a record for the corresponding portal user on the _Users_ (SM201010) form of Acumatica ERP. This user can then sign in to the portal and access forms based on the assigned roles. 

 In this chapter, you’ll learn: 

- Which predefined user roles are provided in the Modern Customer Portal and what access rights they     include 

- How to assign roles to contacts who will use the portal 

 This functionality is available only if the Modern Customer Portal feature is enabled on the Enable/ Disable Features (CS100000) form in Acumatica ERP. 

### Modern Customer Portal: Access Rights Through Predefined Roles 

 The Modern Customer Portal uses predefined roles to control what each portal user can see and do. Each role defines a specific set of access rights, helping protect data while keeping the portal experience focused and easy to manage. 

 This topic explains how the predefined portal roles control user access. You’ll also find reference information on each predefined role to help you determine which roles you want to assign to portal users. 

#### Role-Based Access in the Portal 

 The Modern Customer Portal uses a role-based access model. When a portal user signs in, their assigned roles determine what they can do and which workspaces and forms they can access. By assigning roles that match with each user’s job responsibilities, you give them the appropriate access to the catalog, orders, cases, and sensitive financial information. 

 A contact needs to be defined for a customer employee so that roles can be assigned in either of these ways: 

- **In Acumatica ERP:** On the _Contacts_ (CR302000) form, you (or another Acumatica ERP administrator) assign     one or more roles to a contact. This may be done in response to a case submitted by a portal user. 

 A matching portal user is created on the Users (SM201010) form of Acumatica ERP when an administrator specifies the user type on the Contacts form. 

- **In the Modern Customer Portal:** A portal manager assigns one or more roles to a contact on the Company     Contacts (SP201020) form. 

 A corresponding portal user is automatically created on the Users form of Acumatica ERP when the portal manager assigns roles to a contact in the Modern Customer Portal. 


<!-- PAGE_BREAK -->
 Assigning Roles to Portal Users | 22 

#### Overview of Portal Roles 

 The following table shows the predefined portal roles, their access rights, and the forms a user with the role can access (if these forms are available in the portal). 

 Portal Role Access Rights Forms a User with the Role Can Access 

 Portal User Basic access to the portal for a general user. The user can view and edit their own profile but cannot access company-level data. 

 Every user must be assigned this role to sign in to the Modern Customer Portal. 

- Homepage (SP000000) 

- My Profile (SP101000) 

 Portal Admin Full administrative rights to all portal configuration and settings. 

 This role is intended for Acumatica ERP administrators of the portal owner. It can’t be assigned to external users or linked to any contact, and it isn’t associated with a specific customer account. 

 Portal administrators cannot access financial documents or customer-specific data. Although they can access all portal workspaces (as users with the Portal Manager role can), this access is limited to setup and maintenance. 

 None 

 Customer Portal Manager 

 Full access to portal functionality (including ordering, support, and financial forms). This user can create payment methods and contacts in the portal. 

 This role is intended for the customer’s primary coordinator, who needs broad visibility to portal forms. 

- Company Profile (SP201000) 

- Company Contact (SP201020) 

- Catalog (SP504001) 

- Cart (SP504003) 

- Review Order (SP504004) 

- Orders (SP504010) 

- Order (SP504000) 

- Balance Overview (SP314010) 

- Payments (SP334000) 

- Invoice Payments (SP314001) 

- Pay (SP314002) 

- Statement History (SP324010) 


<!-- PAGE_BREAK -->
 Assigning Roles to Portal Users | 23 

 Portal Role Access Rights Forms a User with the Role Can Access 

- Cases (SP401010) 

- Case (SP401000) 

 Customer Portal Company Manager 

 Access to the company-level settings, including: 

- Managing the company profile 

- Viewing contacts and users 

- Reviewing and updating pay-     ment methods 

- Company Profile (SP201000) 

 Customer Portal Contact Manager 

 Access to the company-level settings in the portal, including: 

- Viewing and managing contacts     and users 

- Creating contacts 

- Company Profile (SP201000) 

- Company Contact (SP201020) 

 Customer Portal Order Manager 

 Access to the catalog and full order history. This user can: 

- Place orders and view their sta-     tuses 

- Manage order-related activities 

- Pay orders by using configured     payment methods 

- Catalog (SP504001) 

- Cart (SP504003) 

- Review Order (SP504004) 

- Orders (SP504010) 

- Order (SP504000) 

- Pay (SP314002) 

 Customer Portal Case Manager 

 Access rights to create and manage support cases. This user can: 

- Submit new cases 

- Reply to existing cases 

- View case statuses 

- Cases (SP401010) 

- Case (SP401000) 

 Customer Portal Financial Manager 

 Access to the financial information, including: 

- Viewing invoices, balances, and     statements 

- Making payments 

- Balance Overview (SP314010) 

- Payments (SP334000) 

- Invoice Payments (SP314001) 

- Pay (SP314002) 

- Statement History (SP324010) 

#### Learn More 

 To learn how to assign roles to contacts, see Modern Customer Portal: Role Assignment in Acumatica ERP. 

### Modern Customer Portal: Role Assignment in Acumatica ERP 

 Aer a portal manager creates a contact, the contact must be assigned access rights before the corresponding portal user can sign in to the system. This can happen in one of these ways: 

- You or another Acumatica ERP administrator assign the role or roles to the contact based on a portal     manager’s request. Below you’ll read about this scenario. 


<!-- PAGE_BREAK -->
 Assigning Roles to Portal Users | 24 

- A portal manager assigns the role to the contact on their own, as described in _Modern Customer Portal: Role_     _Assignment in the Portal_. **At a Glance:** Assigning Access Rights in Acumatica ERP 

1. Receive a case requesting the assignment of one or more roles to the contact. 

2. Assign the appropriate user type and the requested role or roles to the contact. 

3. Save the record. The system automatically creates a user account for the contact. 

 Who performs these steps: An Acumatica ERP administrator. 

#### Assigning Roles to a Contact in Acumatica ERP 

 Suppose that you’ve received an email notification that the portal manager has created a case for you requesting role assignment for a contact. The submitted case is visible in both the portal and Acumatica ERP. 

 To find the contact quickly, first open the customer on the Customers (AR303000) form (Item 1). Then on the Contacts tab (Item 2), click the link in the Contact column (Item 3). 

 Figure: The link to view the contact in Acumatica ERP 

 The Contacts (CR302000) form opens with the contact selected. On the Access to Portal tab (Item 1 below), select the Portal External User user type (Item 2). 

 In the User Roles section, select the check boxes that correspond to the roles the portal manager requested (Item 3): 

- The _Portal User_ role. 

 By default, every contact must be assigned this role so that the employee can sign in to the Modern Customer Portal. 

- At least one role that matches the employee’s responsibilities (see below). 


<!-- PAGE_BREAK -->
 Assigning Roles to Portal Users | 25 

 Figure: The contact’s roles 

 Save your changes, which causes the system to create a user account on the Users (SM201010) form. 

 If you select only the Portal User role for a contact, this user will see only the homepage and My Profile (SP101000) forms in the portal. 

#### Viewing Portal Users 

 Aer you create portal users, they appear on the Portal Users tab of the Portals (SP701000) form. The list shows each user’s roles, email address, linked business account (customer), and status (Items 1–4 below). 

 You can click links (Item 2 and 5) to view or update information about the customer and the contact on the Business Accounts (CR303000) and Contacts (CR302000) forms. 

 Figure: List of the portal’s users 

#### What's Next? 

 Now that the portal user has been assigned the needed role or roles, they can sign in to the Modern Customer Portal and perform tasks based on their roles. 


