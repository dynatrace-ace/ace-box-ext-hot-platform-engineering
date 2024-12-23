## Backstage: New Component from Template

### Create new component from template

![Backstage New Component](../../../assets/images/03_01_backstage_new_component.png)

Using the links on the Dynatrace Training dashboard, navigate to Backstage in your browser.

1. Click on `Create` to create a new component with Backstage.  From the available Templates, locate the `Create a new Application` Template and click on `Choose`.

2. Begin creating a new application by selecting a Project.  Choose `simplenodservice` as the Project.  Click `Next`.

3. Enter your assigned team identifier, such as `team01` or `team30` given by the intructors.  Give your team a name, something unique or simply `Team XYZ`.  Enter a fake team email address, such as `team01@dynatrace.training` or `team30@dynatrace.training` based on your given team identifier.  Emails will not be sent to these addresses as part of this lab.  Click `Next`.

4. Leave the `Application Version`, `Software Lifecycle Stage`, `DORA metric tracking enabled`, `Include Security scans`, and `Include Dynatrace Configuration` at their default values.  Click `Review`.

5. Verify the information you entered is correct.  Click `Create` to create your new component.

Backstage will now execute a series of steps that will
1. **Fetch** the files from our template Git repository
2. **Replace** placeholders with the values we entered in the wizard
3. **Publishes** those changed files as a new repository in GitLab
4. **Sends** an SDLC Event to Dynatrace
5. **Registers** this newly created app in Backstage to show up in the catalog