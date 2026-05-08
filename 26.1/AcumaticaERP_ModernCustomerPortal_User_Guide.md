## User Guide 

# Modern Customer Portal User Guide 

# 2026 R1 


<!-- PAGE_BREAK -->
 Contents | 2 

## Contents 

 Copyright...............................................................................................................................................3 

 Modern Customer Portal for Users........................................................................................................... 4 

 Modern Customer Portal: General Information......................................................................................... 5 

 Adding Contacts and Payment Methods................................................................................................... 6 

 Modern Customer Portal: Contact Creation.....................................................................................................6 

 Modern Customer Portal: Creation of Payment Methods................................................................................8 

 Assigning Roles to Users in the Portal.................................................................................................... 11 

 Modern Customer Portal: Access Rights Through Predefined Roles.............................................................11 

 Modern Customer Portal: Requesting of Role Assignment........................................................................... 13 

 Modern Customer Portal: Role Assignment in the Portal..............................................................................14 

 Managing Cases.................................................................................................................................... 16 

 Modern Customer Portal: Case Management................................................................................................ 16 

 Browsing the Catalog and Placing Orders............................................................................................... 20 

 Modern Customer Portal: Browsing the Catalog........................................................................................... 20 

 Modern Customer Portal: Placing and Reviewing Orders............................................................................. 24 

 Creating Payments and Viewing Balances...............................................................................................29 

 Modern Customer Portal: Paying Sales Orders and Invoices........................................................................ 29 

 Modern Customer Portal: Working with Financial Data................................................................................ 34 


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
 Modern Customer Portal for Users | 4 

## Modern Customer Portal for Users 

 The Modern Customer Portal gives your company a dedicated, user-friendly site to interact with the portal owner— for example, placing orders and submitting support cases. 

 The portal owner is the company that you communicate with by using the Modern Customer Portal. 

 This guide describes how to use the Modern Customer Portal. Your capabilities depend on the roles assigned to you. 

 The guide explains how to: 

- Create and manage contact records for other employees in your company who will use the portal 

- Assign predefined roles to contacts so they can perform only tasks that fit their responsibilities 

- Enter and manage payment methods 

- Browse the catalog, place orders, and review order details 

- Make payments and review financial information 

- Submit and track support cases 


<!-- PAGE_BREAK -->
 Modern Customer Portal: General Information | 5 

## Modern Customer Portal: General Information 

 The Modern Customer Portal provides access to selected data from the portal owner’s Acumatica ERP system in a modern, intuitive interface. Through the portal, users in your company can browse products, place orders, make payments, and communicate with the portal owner, depending on their assigned roles. 

#### Roles and User Access 

 To sign in to the portal, each user must be defined as a contact of your company and assigned at least one predefined role. A portal user’s roles determine what they can see and do in the Modern Customer Portal. 

 In this guide, portal users refers to employees of your company who use the Modern Customer Portal, regardless of their role. 

 Roles can be set up in either of the following ways: 

- Directly in the Modern Customer Portal by a portal manager—an employee of your company with access     rights to perform administrative tasks. 

- By request, through a case created in the portal. An Acumatica ERP administrator assigns the requested     roles, which are applied in the portal. 

#### Portal Capabilities 

 Portal users can do the following, depending on their assigned roles: 

- Enter your company’s payment methods—either in advance or while placing a sales order or paying an     invoice. 

- Create and track support cases to the portal owner and communicate through case messages. 

- Place and manage orders efficiently. You can browse products, check prices and availability, and reorder     past purchases. 

- Make payments for open documents and review financial data to stay on top of your company’s account     status. The Modern Customer Portal gives your company autonomy, transparency, and convenience in your interactions with the portal owner. 

 You can use the following portal functionality only if an administrator of the portal owner has enabled the noted features on the Enable/Disable Features form of Acumatica ERP: 

- Portal functionality: The _Modern Customer Portal_ feature 

- Inventory management: The _Inventory and Order Management_ feature In addition, some functionality is available only if the administrator has selected the noted check boxes on the **General** tab of the _Portals_ (SP701000) form of Acumatica ERP for the portal: 

- **B2B Ordering** 

- **Case Management** 

- **Financials** 

- **Payments** The check boxes should also be selected for the available portal forms in these categories. 


<!-- PAGE_BREAK -->
 Adding Contacts and Payment Methods | 6 

## Adding Contacts and Payment Methods 

 Before assigning roles in the Modern Customer Portal, you—if you’re an authorized portal user—may need to perform these setup steps: 

- Adding contact records for employees who will be using the portal, if these don’t already exist. (You can add     additional contacts at any time.) 

- Entering your company’s payment methods. Portal users can also enter new payment methods as they pay     sales orders and invoices. In this chapter, you’ll learn how to perform both of these tasks. 

 This functionality is available if the following are true in Acumatica ERP: 

- The **Admin** and **System** check boxes are selected for the portal on the _Portals_ (SP701000) form 

- The _Modern Customer Portal_ feature is enabled on the _Enable/Disable Features_ (CS100000)     form If expected functionality isn’t available, contact your company’s portal manager. The portal manager can work with the portal owner to review configuration settings, if needed. 

### Modern Customer Portal: Contact Creation 

 You may need to give more employees in your company access to the Modern Customer Portal. To do this, you create contacts —records for employees of your company who will use the portal. Once the needed roles are assigned to these contacts, they can use the portal. 

 In this topic, you’ll learn how to create these contacts in the Modern Customer Portal. 

 Who does this: An authorized portal user of a company using the Modern Customer Portal. This user must have the Customer Portal Manager or Customer Portal Contact Manager role. 

#### Adding a Contact 

 To create a contact who will use the portal: 

1. Open the _Company Profile_ (SP201000) form in the Modern Customer Portal. 

2. In the **Contacts** section, click **Add New Contact**. 


<!-- PAGE_BREAK -->
 Adding Contacts and Payment Methods | 7 

 Figure: The button to create a contact 

 This section may show contacts that have been entered for your company by the portal owner. 

3. On the Company Contact (SP201020) form, which opens, enter the basic contact information—the portal     user's first and last name, email address, and phone number—and save your changes (see Items 1–2 below).     If needed, enter address settings (Item 3), which will be used when this contact places orders and the items     are shipped. 


<!-- PAGE_BREAK -->
 Adding Contacts and Payment Methods | 8 

 Figure: The contact’s basic information 

 When you save the contact: 

- The system creates the contact in Acumatica ERP and makes it visible in both Acumatica ERP and the     Modern Customer Portal. 

- The **Portal Access** section becomes available (Item 4). You can use it to assign roles to the contact     yourself or request the role assignment from the Acumatica ERP administrator. 

 You can assign roles to contacts only if you have the Customer Portal Manager or Customer Portal Contact Manager access rights. 

#### What's Next? 

 Now that you’ve created a contact for the portal user, you can assign one or more portal roles to them directly in the Modern Customer Portal. For more information, see Modern Customer Portal: Role Assignment in the Portal. 

 Alternatively, you can submit a case to the Acumatica ERP administrator and request role assignment (see Modern Customer Portal: Requesting of Role Assignment ). 

 For more information about portal roles, see Modern Customer Portal: Access Rights Through Predefined Roles. 

### Modern Customer Portal: Creation of Payment Methods 

 In the Modern Customer Portal, you can create, view, and quickly update your company's payment methods. 

 In this topic, you’ll learn how portal users can create payment methods. 

 Who does this: An authorized portal user of a customer using the Modern Customer Portal. This user typically has the Customer Portal Manager or Customer Portal Company Manager role. 

#### Creating a Payment Method 

 You create a payment method on the Company Profile (SP201000) form of the Modern Customer Portal. 

 In the Payment Methods section, click Add New Record (see below). 


<!-- PAGE_BREAK -->
 Adding Contacts and Payment Methods | 9 

**_Figure: The Add New Record button_** 

In the **Create New Card** dialog box, enter the settings for the card and click **Submit**. 


<!-- PAGE_BREAK -->
 Adding Contacts and Payment Methods | 10 

 Figure: The card’s settings 

 The new payment method appears in the Payment Methods section of the Company Profile form. In this section, you can set a payment method as the default one or delete it. 

#### What's Next? 

 You—and other portal users—can place orders and make payments in the Modern Customer Portal. 

 For more information, see Modern Customer Portal: Placing and Reviewing Orders and Modern Customer Portal: Paying Sales Orders and Invoices. 


<!-- PAGE_BREAK -->
 Assigning Roles to Users in the Portal | 11 

## Assigning Roles to Users in the Portal 

 Roles determine which forms and actions are available to portal users in the Modern Customer Portal. Each role includes a defined set of access rights, and every portal user must have at least one role. Roles can be assigned to portal users by: 

- An administrator in Acumatica ERP 

- An authorized portal user directly in the Modern Customer Portal When a contact—an employee of your company who will use the portal—is created, it becomes visible in both Acumatica ERP and the Modern Customer Portal. Then you assign one or more roles to the contact, causing a record for the corresponding portal user to be created on the _Users_ (SM201010) form of Acumatica ERP. The user can then sign in to the portal and access forms based on the assigned roles. 

 In this chapter, you’ll learn: 

- Which predefined roles are provided in the Modern Customer Portal and what access rights they include 

- How to create a case to ask the Acumatica ERP administrator to assign roles 

- How to assign roles to contacts directly in the Modern Customer Portal 

 This functionality is available only if the Modern Customer Portal feature is enabled on the Enable/ Disable Features (CS100000) form of Acumatica ERP. 

 If expected functionality isn’t available, contact your company’s portal manager. The portal manager can work with the portal owner to review configuration settings, if needed. 

### Modern Customer Portal: Access Rights Through Predefined Roles 

 The Modern Customer Portal uses predefined roles to control what each portal user can see and do. Each role defines a specific set of access rights, helping protect data while keeping the portal experience focused and easy to manage. 

 This topic explains how the predefined portal roles control user access. You’ll also find reference information on each predefined role to help you determine which roles you want to assign to portal users. 

#### Role-Based Access in the Portal 

 The Modern Customer Portal uses a role-based access model. When a portal user signs in, their assigned roles determine what they can do and which workspaces or forms they can access. By assigning roles that match with each user’s job responsibilities, you give them the appropriate access to the catalog, orders, cases, and sensitive financial information. 

 A contact of your company can be assigned roles in either of these ways: 

- In Acumatica ERP: On the _Contacts_ (CR302000) form, an administrator assigns one or more roles to a     contact. (This may be done in response to a case submitted by a portal user.) 

 A matching portal user is created on the Users (SM201010) form of Acumatica ERP when an administrator specifies the user type on the Contacts form. 

- In the Modern Customer Portal: A portal manager assigns one or more roles to a contact on the Company     Contacts (SP201020) form. 


<!-- PAGE_BREAK -->
 Assigning Roles to Users in the Portal | 12 

 A corresponding portal user is automatically created on the Users form of Acumatica ERP when the portal manager assigns roles to a contact in the Modern Customer Portal. 

#### Overview of Portal Roles 

 The following table shows the predefined portal roles, their access rights, and the forms a user with the role can access (if these forms are available in the portal). 

 Portal Role Access Rights Forms a User with the Role Can Access 

 Portal User Basic access to the portal for a general user. The user can view and edit their own profile but cannot access company-level data. 

 Every user must be assigned this role to sign in to the Modern Customer Portal. 

- Homepage (SP000000) 

- My Profile (SP101000) 

 Customer Portal Manager 

 Full access to all portal functionality (including ordering, support, and financial forms). This user can create payment methods and contacts in the portal. 

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


<!-- PAGE_BREAK -->
 Assigning Roles to Users in the Portal | 13 

 Portal Role Access Rights Forms a User with the Role Can Access 

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

 To learn how to assign roles to contacts, see Modern Customer Portal: Role Assignment in the Portal. 

### Modern Customer Portal: Requesting of Role Assignment 

 Aer you create a contact, access rights must be assigned before the user can sign in to the portal. If you prefer not to assign roles yourself, you can create a case to request role assignment from the Acumatica ERP administrator, as described in this topic. (You can also assign roles directly, as described in Modern Customer Portal: Role Assignment in the Portal .) 

 Who does this: An authorized portal user of a customer using the Modern Customer Portal. This user must have the Portal Manager or Portal Contact Manager role. 

 For detailed information about submitting and managing cases, see Modern Customer Portal: Case Management. 

#### Creating a Case to Request Role Assignment 

 Aer you create a contact in the customer portal, the contact must be assigned roles so that the user can sign in. 

 To create a case for the Acumatica ERP administrator, open the Case (SP401000) form of the portal and fill in the request’s settings. 


<!-- PAGE_BREAK -->
 Assigning Roles to Users in the Portal | 14 

 Figure: A case requesting the assignment of access rights 

 When you submit the case: 

- The case becomes visible in both the portal and Acumatica ERP. 

- The administrator receives an email notification about the case. 

#### What's Next? 

 Aer the administrator assigns roles to the contact, the contact can sign in to the portal and access forms based on the assigned roles. 

 If you—or another portal user in your company—want to assign roles directly in the future, see Modern Customer Portal: Role Assignment in the Portal. 

### Modern Customer Portal: Role Assignment in the Portal 

 Aer you create a contact, you must assign roles before the employee can sign in to the system. These roles determine access rights. 

 You can assign roles directly in the Modern Customer Portal, as described in this topic, or request assistance from the Acumatica ERP administrator. 

 At a Glance: Assigning Access Rights to the Portal 

1. Open the contact in the Modern Customer Portal. 

2. Assign one or more roles to the contact. 

 Who does this: An authorized portal user of a company using the Modern Customer Portal. This user must have the Customer Portal Manager or Customer Portal Contact Manager role. 

 This simple process is described below. 


<!-- PAGE_BREAK -->
 Assigning Roles to Users in the Portal | 15 

#### Assigning Roles to a Contact in the Portal 

 On the Company Contact (SP201020) form of the Modern Customer Portal, select the contact you want to assign roles to. In the Portal Access section, click the Grant Access button. 

 You can open the Company Contact form by using the Company Profile (SP201000) form. To do that, in the Contacts section, just click the contact’s name. 

 Then select the check boxes for the appropriate roles, which are: 

- The _Portal User_ role. 

 Every contact must be assigned this role to sign in to the Modern Customer Portal. 

- At least one additional role that matches the employee’s position and assigned responsibilities. 

 Figure: Assignment of user roles 

 For more information, see Modern Customer Portal: Access Rights Through Predefined Roles. 

 Save your changes. The system creates the contact’s user account on the Users (SM201010) form of Acumatica ERP. 

 If you select only the Portal User role for a contact, this user can access only the Homepage (SP000000) and My Profile (SP101000) forms in the portal. 

#### What's Next? 

 The portal user can now sign in to the Modern Customer Portal and perform tasks based on the assigned roles. The remaining chapters of this guide describe these tasks. 


<!-- PAGE_BREAK -->
 Managing Cases | 16 

## Managing Cases 

 If you’re a portal user, you can create and manage cases in the Modern Customer Portal. 

 In this chapter, you'll learn how to: 

- Create a case for assistance with the portal or the catalog 

- Update the case in the Modern Customer Portal 

 This functionality is available if the following are true in Acumatica ERP: 

- The _Modern Customer Portal_ and _Case Management_ features are enabled on the _Enable/Disable_     _Features_ (CS100000) form 

- The **Case Management** check box is selected and the functionality has been configured on the     _Portals_ (SP701000) form. If expected functionality isn’t available, contact your company’s portal manager. The portal manager can work with the portal owner to review configuration settings, if needed. 

### Modern Customer Portal: Case Management 

 The Case (SP401000) and Cases (SP401010) forms in the Modern Customer Portal are integrated with Acumatica ERP’s case management functionality. You can submit and manage cases in the portal, and employees of the portal owner’s support team can view and manage these cases in Acumatica ERP. 

 On the Case form, you can: 

- Create and submit cases 

- Check the status of existing cases 

- Communicate with the support team through case messages This topic explains how you can create and update cases in the Modern Customer Portal. 

 At a Glance: Portal Case Management 

- Create a case in the Modern Customer Portal. 

- Send a case message to the Acumatica ERP support team. **Who does this:** An authorized portal user of a company using the Modern Customer Portal. This user typically has the _Customer Portal Manager_ or _Customer Portal Case Manager_ role. 

 These tasks are described in the next sections. 

#### Creating a Case 

 The Cases (SP401010) form of the Modern Customer Portal is the starting point for creating cases and viewing all cases your company’s employees have submitted through the portal. Click the Add New Record button to create a case. 


<!-- PAGE_BREAK -->
 Managing Cases | 17 

**_Figure: The button for adding a case_** 

Then on the _Case_ (SP401000) form, which opens, fill in the case’s settings. In the **Summary** box, type a brief description of the case. On the **Details** tab, enter a detailed description of the issue or request. 

**_Figure: The case's settings_** 

Then click **Submit** to submit the case to the portal owner and display it in their system. The system will assign an identifier to the case and notify the portal owner’s support team. 


<!-- PAGE_BREAK -->
 Managing Cases | 18 

#### Updating a Case 

 Once you’ve created a case, you can track its status, review it, and update its settings in the Modern Customer Portal. 

 You can also continue communicating with the Acumatica ERP support team about the case. On the form toolbar of the Case (SP401000) form, you click Send Message and enter your message in the dialog box. 

 Figure: Creation of a message for the case 

 On the Activities tab, you can view all messages you've sent and received for the case. 


<!-- PAGE_BREAK -->
 Managing Cases | 19 

**_Figure: Case messages on the Activities tab_** 

To close a case or reopen it, click **Close Case** or **Reopen Case**. 

**_Figure: Buttons for closing and reopening a case_** 


<!-- PAGE_BREAK -->
 Browsing the Catalog and Placing Orders | 20 

## Browsing the Catalog and Placing Orders 

 In the Modern Customer Portal, authorized portal users can browse the catalog, view available items and their details, add items to the cart, and place orders. 

 In this chapter, you’ll learn how you can: 

- Browse the catalog and view item details 

- Place an order 

- Review order details in the Modern Customer Portal 

 This functionality is available if the following are true in Acumatica ERP: 

- The _Modern Customer Portal_ and _Inventory and Order Management_ features are enabled on the     _Enable/Disable Features_ (CS100000) form 

- The **B2B Ordering** check box is selected and the functionality has been configured on the     _Portals_ (SP701000) form. If expected functionality isn’t available, contact your company’s portal manager. The portal manager can work with the portal owner to review configuration settings, if needed. 

### Modern Customer Portal: Browsing the Catalog 

 In the Modern Customer Portal, you can browse a catalog of items, view key information about any item, and add items directly to the cart. The catalog includes search and filtering capabilities along with real-time inventory visibility as you shop. 

 This topic explains how to browse the catalog and add items to the cart in the Modern Customer Portal. 

 Who does this: An authorized portal user of a company that uses the Modern Customer Portal. This task is typically done by a user with the Customer Portal Manager or Customer Portal Order Manager role who’s involved in purchasing. 

#### Catalog Overview 

 The Modern Customer Portal catalog is designed for efficient browsing and ordering. 


<!-- PAGE_BREAK -->
 Browsing the Catalog and Placing Orders | 21 

 Figure: The portal catalog 

 In the catalog, you can: 

- **Search and filter items:** Use the search bar and filters to find items by using keywords, categories, or stock     status. 

- **View real-time inventory visibility:** See warehouse-specific item availability. As goods are moved,     inventory data in the catalog is updated instantly. 

- **Add items directly to the cart:** Select the quantity, warehouse, and unit of measure to add items to the cart     without leaving the catalog. The cart in the top pane is updated immediately. 

- **View item details:** Click any item’s image to view more details without leaving the form. 

#### Starting Your Order 

 To browse the catalog and add needed items to the cart in the Modern Customer Portal, do the following: 

1. Open the Catalog (SP504001) form. 

2. At the top of the form, notice the Search box (Item 1 below), the Filter List menu (Item 2), selection boxes     (Item 3), Add Quick Filter button (Item 4), and More button (Item 5). You can use these elements to find items     faster or narrow the items shown. 

 Figure: Elements for finding items on the Catalog form 


<!-- PAGE_BREAK -->
 Browsing the Catalog and Placing Orders | 22 

3. Click an item’s image (Item 1 below). View the item’s description in the **Item Details** dialog box. 

4. Optional: Change the default warehouse, unit of measure, and quantity if you’re purchasing the item. 

5. Click **Add to Cart** (Item 3). 

 You can also add an item to the cart directly on the Catalog form by clicking Add to Cart below the item’s image (Item 2). 

 Figure: Buttons for adding an item to the cart 


<!-- PAGE_BREAK -->
 Browsing the Catalog and Placing Orders | 23 

6. Repeat the three previous steps until you’ve added all needed items. 

#### Viewing Your Cart 

 At any time, you can click the Cart button on the right side of the top pane, shown below, to open the Cart (SP504003) form. 

 On this form, you can: 

- View the items you’ve added to the cart, along with their quantities, units of measure, prices, warehouses,     and totals 

- Update quantities 

- Change units of measure or warehouses (if applicable) 

- Remove items 

 Figure: Your cart 


<!-- PAGE_BREAK -->
 Browsing the Catalog and Placing Orders | 24 

 As you shop, the system instantly updates your totals, so the Cart form always shows an accurate summary of your order. Also, the Cart button shows the number of items and the order total. 

#### What's Next? 

 To learn how to place your order, see Modern Customer Portal: Placing and Reviewing Orders. 

### Modern Customer Portal: Placing and Reviewing Orders 

 In the Modern Customer Portal, you can quickly review orders, make adjustments, enter or confirm shipping and payment details, and place the order. 

 In this topic, you’ll learn how to place orders in the Modern Customer Portal. 

 At a Glance: Placing Orders 

1. Open the cart, review the added items, and proceed to checkout 

2. Review the order’s details on the Review Order (SP504004) form, and place the order 

3. View (and optionally, print or cancel) the placed order on the Order (SP504000) form 

 Who does this: An authorized portal user of a company that uses the Modern Customer Portal. This task is typically done by a user with the Customer Portal Manager or Customer Portal Order Manager role who’s involved in purchasing. 

#### About the Cart 

 As you shop in the Modern Customer Portal, you can: 

- **View key order details and quickly go to your cart:** The cart button (Item 1 below) is always visible on the     right side of the top pane for users with the _Customer Portal Manager_ and _Customer Portal Order Manager_     roles. It shows the current number of items and total—and updates these values as you add items. You can     click the button to open the cart. 

- **Modify your cart:** You can remove items, adjust quantities, and select a warehouse or unit of measure     (UOM) for an item, if applicable. The cart instantly shows refreshed totals for the item and the order as a     whole (Items 2–3). 

 Figure: Capabilities for working with the cart 


<!-- PAGE_BREAK -->
 Browsing the Catalog and Placing Orders | 25 

#### Placing an Order 

 Suppose that you’ve added some items to the cart, as described in Modern Customer Portal: Browsing the Catalog. To place an order in the portal, do the following: 

1. Click the **Cart** button in the top pane (Item 1 below) to open the Cart (SP504003) form, also shown below. 

2. Review the items and click **Proceed to Checkout** (Item 2). 

 Figure: The Proceed to Checkout button 

3. On the Review Order (SP504004) form, which opens (see below), review the order’s details and click **Place**     **Order** (Item 1).     Before you place the order, you can: 

- Change shipment and billing details (Item 2) 

- Change the payment method (Item 3) or add a new one on the fly 

- Enter your company’s order number and description (Item 4) 

 Figure: Final review of the order 


<!-- PAGE_BREAK -->
 Browsing the Catalog and Placing Orders | 26 

 The system processes the order and submits it to the portal owner. The order is visible in both the Modern Customer Portal and Acumatica ERP. 

The Order (SP504000) form opens, showing the order (Item 1 below). If needed, you can print or cancel it (Items 2 and 4). 

**_Figure: The submitted order_** 


<!-- PAGE_BREAK -->
 Browsing the Catalog and Placing Orders | 27 

 Need to create an order that’s similar to or the same as a past order? Start by opening the past order. Then click Copy Order to Cart (Item 3), and all items and quantities will be added to your cart. 

#### Viewing All Orders 

 On the Orders (SP504010) form, you can use intuitive filter tabs to view: 

- Unpaid orders 

- Orders with the _Open_ status 

- All orders your company has placed You can also use the Search box to quickly find a particular order. 

 Figure: Elements for finding orders easily 


<!-- PAGE_BREAK -->
 Browsing the Catalog and Placing Orders | 28 

#### What’s Next? 

 To learn how to make payments directly through the Modern Customer Portal, see Modern Customer Portal: Paying Sales Orders and Invoices. 


<!-- PAGE_BREAK -->
 Creating Payments and Viewing Balances | 29 

## Creating Payments and Viewing Balances 

 In the Modern Customer Portal, if you’re an authorized portal user, you can make payments and view your company’s balances, statements, and financial documents. By handling these tasks in the portal, you can save time and keep the company’s financial information up to date. 

 In this chapter, you'll learn how you can: 

- Make full and partial payments for sales orders or invoices 

- Review financial documents, statements, and balances 

 This functionality is available if the following are true in Acumatica ERP: 

- The _Modern Customer Portal_ feature is enabled on the _Enable/Disable Features_ (CS100000)     form 

- The **Financials** and **Payments** check boxes are selected and the functionality has been     configured on the _Portals_ (SP701000) form. If expected functionality isn’t available, contact your company’s portal manager. The portal manager can work with the portal owner to review configuration settings, if needed. 

### Modern Customer Portal: Paying Sales Orders and Invoices 

 In the Modern Customer Portal, you can make payments for orders and invoices by using saved payment methods or adding new ones on the fly. In this topic, you’ll learn how to do this. 

 At a Glance: Making Payments 

1. Open either the Orders (SP504010) form for sales orders or the _Balance Overview_ (SP314010) form for sales     invoices. 

2. Do one of the following: 

- Select the sales orders or invoices to be paid now and then click **Proceed to Pay**. 

- Click **Proceed to Pay All**. 

3. On the _Pay_ (SP314002) form, complete the payment. 

 Who does this: An authorized portal user of a company that uses the Modern Customer Portal. This task is typically done by a user with the Customer Portal Manager , Customer Portal Financial Manager , or Customer Portal Order Manager role. 

 Let’s take a closer look at how this process works. 

#### Starting to Pay Sales Orders 

 In the Modern Customer Portal, you start paying open sales orders on the Orders (SP504010) form. Do either of the following: 

- Select the check boxes for the open orders you want to pay and click **Proceed to Pay** (see below). 

 You can make payments for selected documents only if they have the same currency. If you select a check box for a document in one currency, the check boxes for documents in other currencies become unavailable. 


<!-- PAGE_BREAK -->
 Creating Payments and Viewing Balances | 30 

 Figure: Selection of orders for payment 

- Click **Proceed to Pay All** to pay all open orders that are listed on the filter tab. 

 Figure: The Proceed to Pay All button 

 When you click Proceed to Pay or Proceed to Pay All , the Pay form opens. 

#### Completing the Payment 

 On the Pay (SP314002) form, you complete the payment process. Do either of the following: 

- Make full payments for all listed orders: Select the payment method (Item 1 below), enter a payment     description (Item 2), review the listed sales orders (Item 3), and click **Pay** (Item 4). 

 Figure: Completion of a full payment 


<!-- PAGE_BREAK -->
 Creating Payments and Viewing Balances | 31 

 In the Payment Method section (Item 1), you can create a payment method without leaving the form. To do this, click Add New Card. In the Create New Card dialog box, enter the settings for the payment and click Submit. 

- Make partial payments. For any sales order, enter the amount you want to pay and click **Pay**. 

 Figure: Completion of a partial payment 


<!-- PAGE_BREAK -->
 Creating Payments and Viewing Balances | 32 

#### Starting to Pay Invoices 

 In the Modern Customer Portal, you can pay any number of open invoices. 

 To begin this process, open the Balance Overview (SP314010) form. On the Open Documents tab, select the check boxes for the invoices you want to pay (Item 1 below) and click Proceed to Pay (Item 3). If you want to pay all listed invoices, click Proceed to Pay All (Item 2). 

 Figure: Selection of invoices for payment 


<!-- PAGE_BREAK -->
 Creating Payments and Viewing Balances | 33 

 Clicking either button opens the Pay (SP314002) form. 

#### Completing the Invoice Payment 

 On the Pay (SP314002) form, you finish the payment process. Select the payment method, enter a payment description (Items 1–2 below), review the listed invoices (Item 3), and click Pay (Item 4). 

 You can instead make partial payments for invoices: For any invoice, you enter the amount you want to pay (Item 5) and click Pay. 

 Figure: Completion of an invoice payment 


<!-- PAGE_BREAK -->
 Creating Payments and Viewing Balances | 34 

#### Unsuccessful Payments 

 The Modern Customer Portal gives you more control over payments and helps you avoid delays. If a payment attempt fails, you don’t need to start over—you can either retry the payment or change the payment method and submit it again. 

 If a payment isn't completed (for example, due to an authorization error), the system retains your payment details and creates a payment with the Pending Processing status. If the next retry is successful, the system: 

- **For sales orders:** Replaces the failed payment with a new one linked to each processed order 

- **For invoices:** Creates a new payment and removes any previously failed payments linked to each processed     invoice 

#### What's Next? 

 To learn how to view financial information in the portal, see Modern Customer Portal: Working with Financial Data. 

### Modern Customer Portal: Working with Financial Data 

 In the Modern Customer Portal, you can review your company’s financial documents and statements in one place. You can check totals, balances, due dates, and payments to keep track of your company’s finances. 

 In this topic, you’ll learn how to view financial data in the portal. 

 At a Glance: Viewing Financial Data 

- Open the _Balance Overview_ (SP314010) form. Review open and closed invoices, payments, and totals. 

- Optional: Make partial or full payments of invoices. 

- Open the Statement History (SP324010) form to review statements. Open any statement by clicking the     statement date, which is a link, and review the statement's details. 


<!-- PAGE_BREAK -->
 Creating Payments and Viewing Balances | 35 

 Who does this: An authorized portal user of a customer that uses the Modern Customer Portal. This task is typically done by a user with the Customer Portal Financial Manager role. 

 In the next sections, you'll see how to use these capabilities in the portal. 

#### Managing Financial Documents in One Place 

 On the Balance Overview (SP314010) form of the Modern Customer Portal, you can view financial documents (invoices and payments) and totals. 

 You can view the relevant documents and totals without switching forms. By using tabs (Item 1 below), you can view open documents, all invoices, or all payments. By default, documents are sorted by date, with the most recent ones first. To find the documents you need, you can use the search box (Item 2), selection boxes (Item 3), and filters (Item 4). 

 Figure: Elements for finding documents 

 On the All Invoices tab (Item 1 below), you can access invoices (Item 2), credit and debit memos (Items 3 and 4), and overdue charges (Item 5). You can see each document’s due date (if applicable), amount, and balance. Document numbers are displayed as links (Item 6). 


<!-- PAGE_BREAK -->
 Creating Payments and Viewing Balances | 36 

**_Figure: Financial documents and their settings_** 

When you click a link with a document number, the system downloads a printable version of the document to your computer. 


<!-- PAGE_BREAK -->
 Creating Payments and Viewing Balances | 37 

**_Figure: The printable invoice_** 

On the **All Payments** tab (Item 1 below) of the _Balance Overview_ form, you can view payments (Item 2) and prepayments (Item 3). 

**_Figure: Payments and prepayments_** 

To review any payment's settings, you can click its number, which is a link. The payment opens on the Payments (SP334000) form, where you can view its status, date, total, currency, and payment method (Item 1 below). 

In the table, you can view the list of documents to which the payment is applied (Item 2). Click any invoice number (Item 3) to open the Invoice Payments (SP314001) form. On this form, you can view the payment details of an invoice (due date, outstanding amount, total, and applied payments). 


<!-- PAGE_BREAK -->
 Creating Payments and Viewing Balances | 38 

 Figure: Documents a payment is applied to 

#### Making Partial or Full Payments 

 From the Open Documents and All Invoices tabs of the Balance Overview (SP314010) form, you can initiate partial or full payments: Select the document or documents to be paid (Item 1 below) and then click Proceed to Pay (Item 3). 

 You can click Proceed to Pay All (Item 2) to make payments of all open documents listed on the Open Documents tab. 


<!-- PAGE_BREAK -->
 Creating Payments and Viewing Balances | 39 

 Figure: Selection of documents for payment 

 For details on making payments in the Modern Customer Portal, see Modern Customer Portal: Paying Sales Orders and Invoices. 

#### Statement History 

 In the Modern Customer Portal, you can access your company's account statements on the Statement History (SP324010) form. The form shows a chronological list of all issued customer statements (Item 1 below). 

 By default, statements are sorted by date, with the most recent ones first. You can use the search box to find a statement or use filters (Items 2–3). 

 Figure: Your company’s statements 


<!-- PAGE_BREAK -->
 Creating Payments and Viewing Balances | 40 

For each statement, you can view key settings: 

- Its date, which is also a link (Item 1 below) 

- The branch of the company selling the items (Item 2) 

- Its balance (Item 3) 

**_Figure: The settings of each statement_** 

You can click any statement’s date to review its details in a printable document that the system downloads to your computer. In this document, you can see invoices and their due dates, amounts due, and balances as of the statement date. 


<!-- PAGE_BREAK -->
 Creating Payments and Viewing Balances | 41 

**_Figure: The printable customer statement_** 


