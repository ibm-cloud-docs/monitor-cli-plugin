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

The {{site.data.keyword.cloud}} command-line interface (CLI) provides extra capabilities for service offerings. This information describes how you can use the CLI to list list all the service instances for {{site.data.keyword.mon_full_notm}} for an account.
{: shortdesc} 

<!-- Prerequisites: REQUIRED FOR PLUG-INS
This section tells users what's required to use the CLI commands. 
- If your CLI is delivered as part of the core IBM Cloud CLI (not separately installable), this section isn't required. 
- If your CLI is delivered as a plug-in to the core IBM Cloud CLI, include installation commands. If your plug-in requires detailed or lengthy configuration steps, link out to a separate task topic. -->

<!-- Change ID below to match your CLI. -->
## Prerequisites
{: #sysdig-monitor-cli-prereq}

* Install the [{{site.data.keyword.cloud_notm}} CLI](/docs/cli?topic=cli-getting-started).
* Install the {{site.data.keyword.mon_full_notm}} CLI by running the following command:

   ```sh
   ibmcloud plugin install monitoring
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

## ibmcloud sysdig service-instances
{: #service-instances}

Use this command to list {{site.data.keyword.mon_full_notm}} service instances. 

```sh
ibmcloud sysdig service-instances [OPTIONS]
```
{:pre}



### Command options 
{: #service-instances-options}

| Option | Description |
| ------ | ----------- |
|--service-name value, --sn value | Name of the service|
  |--region value, -r value      |    Name of the region, for example, `us-south` or `eu-gb`. If not specified, the targeted region will be used. |
  |-g value             |             Resource Group associated with the hosted service|
  |--all-resource-groups, --arg  |    Services hosted across all resource groups|
  |--long, -l              |          Show additional fields in the output|
  |--quiet, -q           |            Supresses verbose output|
  |--json, -j                |        Produces outut as raw JSON|
   
### Examples
{: #service-instances-examples}

TBD

```sh
xxx
```
{: pre}

### Output
{: #service-instances-output}

The command returns the following output:
```
xxx
```
{: screen}


