<!-- default file list -->
*Files to look at*:

* [RegistrationController.cs](./CS/WebSite/Controllers/RegistrationController.cs)
* [Global.asax](./CS/WebSite/Global.asax)
* [Global.asax.cs](./CS/WebSite/Global.asax.cs)
* [Account.cs](./CS/WebSite/Models/Account.cs)
* [ContactPartial.cshtml](./CS/WebSite/Views/Registration/ContactPartial.cshtml)
* [DatePartial.cshtml](./CS/WebSite/Views/Registration/DatePartial.cshtml)
* [PersonalPartial.cshtml](./CS/WebSite/Views/Registration/PersonalPartial.cshtml)
* [SummaryPartial.cshtml](./CS/WebSite/Views/Registration/SummaryPartial.cshtml)
* [Wizard.cshtml](./CS/WebSite/Views/Registration/Wizard.cshtml)
<!-- default file list end -->
# How to organize Wizard interface within PageControl Extension


<p>This example is the ASP.NET MVC implementation of the <a href="https://www.devexpress.com/Support/Center/p/E3050">How to organize Wizard interface within ASPxPageControl</a> example. It illustrates to organize the so-called wizard interface within the MVC PageControl Extension. It allows you to specify the predefined content of the wizard steps within the TabPages and switching between them via user interface (via clicking the TabPage's header) or programmatically (via API).<br /><br /><strong>Updated: <br /><br /></strong></p>
<p>Starting with v14.1 this example uses jQuery Unobtrusive validation. Please refer to <a href="https://documentation.devexpress.com/#AspNet/CustomDocument12060">Unobtrusive Client Validation</a> to learn more about it.</p>


<h3>Description</h3>

<p>The validation of TagPage's (step's) editors works in the following manner:</p>
<p>Clicking the "Finish" button (a complete wizard step) calls the "ValidateEditors" function and validate form's editors. This function searches TabPage that contains the first invalid editor via the "GetTabIndexWithInvalidaEditor" function. If all editors in all steps are valid, the form is submitted.</p>
<br>
<p>In some scenarios, it is necessary to allow a user to navigate between wizard steps via clicking step's by clicking the steps' headers and sometimes - via clicking "next" / "prev" buttons (steps' headers are hidden). To specify the TabPages' header visibility, manipulate the <a href="http://documentation.devexpress.com/#AspNet/DevExpressWebMvcPageControlSettings_ShowTabstopic"><u>PageControlSettings.ShowTabs</u></a> property.</p>
<br>
<p>The "Show Tabs" checkbox is used for demonstration purposes only. Clicking this checkbox forces submission of the entire form. The corresponding Controller's logic analyzes the checkbox's state and clears the Model's state to avoid server-side editor / Model validation.</p>

<br/>


