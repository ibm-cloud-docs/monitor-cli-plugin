---
 
copyright:
  years:  2018, 2021
lastupdated: "2021-03-10"

subcollection: sysdig-monitor-plugin-cli

keywords: IBM Cloud Monitoring CLI, IBM Cloud Monitoring command line , IBM Cloud Monitoring terminal, IBM Cloud Monitoring shell

---

{:shortdesc: .shortdesc}
{:external: target="_blank" .external}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}


<!-- Title guidance:
Add a title that describes your CLI and includes the base command. Formatting guidelines depend on how your content is delivered:
- As part of the core CLI: Provide a goal-oriented title, such as "Searching and managing the IBM Cloud catalog (ibmcloud catalog)": https://cloud.ibm.com/docs/cli?topic=cloud-cli-ibmcloud_catalog
- As a CLI plug-in: List the name of your CLI, such as "Container Registry CLI (ibmcloud cr): https://cloud.ibm.com/docs/cli?topic=container-registry-cli-plugin-containerregcli
Also provide an appropriate ID above that aligns with your offering name, for example: #container-registry-cli. *All* IDs must be unique across *all* CLI references. -->


# {{site.data.keyword.mon_full_notm}} CLI
{: #sysdig-monitor-cli}

<!-- Short description: REQUIRED
The short description section should include one to two sentences describing why a developer would want to use this cli. This should be conversational style. For search engine optimization, include your offering's CLI name. Keep the {: shortdesc} after the first paragraph so that the framework renders it properly.
Example: -->

The {{site.data.keyword.cloud}} command-line interface (CLI) provides extra capabilities for service offerings. You can use {{site.data.keyword.cloud_notm}} CLI to manage V2 service brokers and templates.
{: shortdesc} 

<!-- Prerequisites: REQUIRED FOR PLUG-INS
This section tells users what's required to use the CLI commands. 
- If your CLI is delivered as part of the core IBM Cloud CLI (not separately installable), this section isn't required. 
- If your CLI is delivered as a plug-in to the core IBM Cloud CLI, include installation commands. If your plug-in requires detailed or lengthy configuration steps, link out to a separate task topic. -->

<!-- Change ID below to match your CLI. -->
## Prerequisites
{: #<cli_name>-cli-prereq}

* Install the [{{site.data.keyword.cloud_notm}} CLI](/docs/cli?topic=cli-getting-started).
* Install the <CLI_name> CLI by running the following command:

   ```sh
   ibmcloud plugin install <cli-plugin>
   ```
   {: pre}
   <!-- Replace the <cli-plugin> above with the name of your CLI plug-in. Run 'ibmcloud plugin repo-plugins' to find the name.-->

<!-- Optionally include any other post-installation configuration that might be required for your service. -->

You're notified on the command line when updates to the {{site.data.keyword.cloud_notm}} CLI and plug-ins are available. Be sure to keep your CLI up to date so that you can use the latest commands. You can view the current version of all installed plug-ins by running `ibmcloud plugin list`.
{: tip}

<!-- Other Prerequisites/Authorization/Environment: OPTIONAL
List any other prerequisites/authorization/environments that are required to use the CLI commands. Or give a brief introduction to the prerequisites/authorization/environments that the CLI commands might use. Use H3 headings (###) as needed to organize your content.
Example: -->

{{site.data.keyword.cloud_notm}} CLI requires Java&trade 1.8.0. You can download the CLI from {{site.data.keyword.cloud_notm}} to use on your local system as a complement to the {{site.data.keyword.cloud_notm}} console.
{: note}

<!-- Command entries: REQUIRED
Directly use the command name as title.  Add an anchor ID, for example, {: #login}, for each command entry. Include a sentence to briefly introduce the command, such as what the command does. 

**Command syntax**: Add the command syntax by using three backticks before and after the syntax (```).

**Command options**: Use a definition list to introduce the options. Make one option a single list item. 
				 
Examples: Include one sentence to describe each example. Use 1 - 3 examples depending on the command's complexity, and use examples that show different parts of the command's functionality. For very complex commands, you can include additional examples, but make sure they're not too repetitive.
* Add the example by using three backticks ahead of and after the example (```)
* For copyable code snippets, multi-line, include {: codeblock} following the last set of backticks. A copy button will display in the framework output.
* For copyable commands, single line, include {: pre} following the last set of backticks. When displayed, it will show "$" at the beginning of the command example and a copy button, but the copy button will include just the command example.

Required command options should be listed without brackets, for example `-a API_ENDPOINT`. Command options that aren't requires should be listed in [] square brackets within the command syntax example., such as `[--org ORG]`.

**Optional options**: Options that aren't required should be placed in the option description's <dt> or <dd> tags, and in [] within the command syntax statement.
	
For example, the following command syntax has the optional options -o, -s and -r.
```
ibmcloud account user-invite USER_EMAIL [-o, --org ORG [--org-role ORG_ROLE] [-s, --space SPACE, --space-role SPACE_ROLE]] [-r, --region REGION]
```

* For each option, include in the option's description what the default behavior is if you don't specify it. For example, "If not specified, the default value is `true`." Not all options have a default value. 
* Surround all values that the user inputs in `backticks` to denote that it's a literal value. For example: "Valid values are `true` or `false`".

**Variables**: Document variables by using all caps.

**Mutually exclusive options**:
In the command syntax statement, to indicate options that are mutually exclusive, use a `|` pipe symbol as shown in the following example:
```
[--resource-group-id RESOURCE_GROUP_ID | --resource-group-name RESOURCE_GROUP_NAME]
```
In this example, `resource-group-id` and `resource-group-name` are exclusive.

**Command output**: If the command has output, include an example of what the user will see. Be sure not to include any real names, account numbers, resource CRNs, API keys, or other sensitive information. Above the command output, include a description of any key pieces that the user might need to pay attention to.

-->

## cloud-cli login
{: #login}

Use this command to log in to {{site.data.keyword.cloud_notm}}. 

```
cloud-cli login -a API_ENDPOINT [--sso] [-u USERNAME] [-p PASSWORD] [--apikey KEY | @KEY_FILE] 
                [--no-iam] [-c (ACCOUNT_ID | ACCOUNT_OWNER_USER_ID) | --no-account] 
		[-g (RESOURCE_GROUP_NAME | RESOURCE_GROUP_ID)]
```

<!-- Remove the command-level Prerequisites section if the command doesn't have any. -->
### Prerequisites
{: #login-prereqs}

### Command options 
{: #login-options}

<dl>
<dt>-a API_ENDPOINT</dt>
<dd>The API endpoint, such as `cloud.ibm.com`. Required.</dd>
<dt>--sso</dt>
<dd>Specify this option to [log in with a federated ID](/docs/iam?topic=iam-federated_id). Using this option prompts you to authenticate with your single sign-on provider and enter a one-time passcode to log in.</dd>
<dt>-u USERNAME</dt>
<dd>The {{site.data.keyword.cloud_notm}} user name.</dd>
<dt>-p PASSWORD</dt>
<dd>The user password.</dd>
<dt>--apikey API_KEY or @API_KEY_FILE_PATH</dt>
<dd>The API key content or the path of an API key file that is indicated by the @ symbol.</dd>
<dt>--no-iam</dt>
<dd>Force authentication with the login server instead of the public IAM.</dd>
<dt>-c ACCOUNT_ID</dt>
<dd>The ID of the target account. This option is exclusive with the `--no account` option.</dd>
<dt>--no-account</dt>
<dd>Forced login without the account. This option isn't recommended, and it is exclusive with the `-c` option.</dd>
<dt>-g RESOURCE_GROUP</dt>
<dd>The name or ID of the target resource group.</dd>
</dl>
   
### Examples
{: #login-examples}

Log in to {{site.data.keyword.cloud_notm}} by entering `tom` for the user ID and `123` for the password.

```sh
cloud-cli login -a cloud.ibm.com -u tom -p 123
```
{: pre}

### Output
{: #command-output}

The command returns the following output:
```
Targeted account tom Account (abc123cf7ca78fb1997fcbd8999106af)
                      
API endpoint:      https://cloud.ibm.com   
Region:            us-south   
User:              tom 
Account:           tom's Account (abc123cf7ca78fb1997fcbd8999106af)   
Resource group:    No resource group targeted, use 'ibmcloud target -g RESOURCE_GROUP'   
CF API endpoint:      
Org:                  
Space:                

Tip: If you are managing Cloud Foundry applications and services
- Use 'ibmcloud target --cf' to target Cloud Foundry org/space interactively, or use 'ibmcloud target --cf-api ENDPOINT -o  ORG -s SPACE' to target the org/space.
- Use 'ibmcloud cf' if you want to run the Cloud Foundry CLI with current IBM Cloud CLI context.
```
{: screen}

## command xxx
{: #anchor_ID}

<!-- Grouping guidance:
If your plug-in has many commands, you can group them logically under H2 (##) headings. Within the groups, commands should be listed alphabetically following the previously described format, but with an extra heading level. 

In the H2, don't repeat the core command, e.g. "`billing` commands". Instead, use a plain-text description, like "Billing and usage". -->

## Logging in
{: #my-cli-login-cmd}

### cloud-cli login
{: #login}

Use this command to log in to {{site.data.keyword.cloud_notm}}. 

```
cloud-cli login -a API_ENDPOINT [--sso] [-u USERNAME] [-p PASSWORD] [--apikey KEY | @KEY_FILE] 
                [--no-iam] [-c (ACCOUNT_ID | ACCOUNT_OWNER_USER_ID) | --no-account] 
		[-g (RESOURCE_GROUP_NAME | RESOURCE_GROUP_ID)]
```

#### Prerequisites
{: #login-prereqs}

#### Command options 
{: #login-options}

<dl>
<dt>-a API_ENDPOINT</dt>
<dd>The API endpoint, such as `cloud.ibm.com`. Required.</dd>
<dt>--sso</dt>
<dd>Specify this option to [log in with a federated ID](/docs/iam?topic=iam-federated_id). Using this option prompts you to authenticate with your single sign-on provider and enter a one-time passcode to log in.</dd>
<dt>-u USERNAME</dt>
<dd>The {{site.data.keyword.cloud_notm}} user name.</dd>
<dt>-p PASSWORD</dt>
<dd>The user password.</dd>
<dt>--apikey API_KEY or @API_KEY_FILE_PATH</dt>
<dd>The API key content or the path of an API key file that is indicated by the @ symbol.</dd>
<dt>--no-iam</dt>
<dd>Force authentication with the login server instead of the public IAM.</dd>
<dt>-c ACCOUNT_ID</dt>
<dd>The ID of the target account. This option is exclusive with the `--no account` option.</dd>
<dt>--no-account</dt>
<dd>Forced login without the account. This option isn't recommended, and it is exclusive with the `-c` option.</dd>
<dt>-g RESOURCE_GROUP</dt>
<dd>The name or ID of the target resource group.</dd>
</dl>
   
#### Examples
{: #login-examples}

Log in to {{site.data.keyword.cloud_notm}} by entering `tom` for the user ID and `123` for the password.

```sh
cloud-cli login -a cloud.ibm.com -u tom -p 123
```
{: pre}

#### Output
{: #command-output}

The command returns the following output.

```
Targeted account tom Account (abc123cf7ca78fb1997fcbd8999106af)
                      
API endpoint:      https://cloud.ibm.com   
Region:            us-south   
User:              tom 
Account:           tom's Account (abc123cf7ca78fb1997fcbd8999106af)   
Resource group:    No resource group targeted, use 'ibmcloud target -g RESOURCE_GROUP'   
CF API endpoint:      
Org:                  
Space:                

Tip: If you are managing Cloud Foundry applications and services
- Use 'ibmcloud target --cf' to target Cloud Foundry org/space interactively, or use 'ibmcloud target --cf-api ENDPOINT -o  ORG -s SPACE' to target the org/space.
- Use 'ibmcloud cf' if you want to run the Cloud Foundry CLI with current IBM Cloud CLI context.
```
{: screen}

### command xxx
{: #anchor_ID}
