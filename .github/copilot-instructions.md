## Copilot instructions for ONTAP alerts documentation

### Repository overview
Product: ONTAP alerts

ONTAP alerts is a NetApp Console service for viewing issues and potential risks in on-premises ONTAP storage environments. It surfaces selected EMS and metric-based alerts for ONTAP clusters. It also links alert and cluster details to ONTAP System Manager. 

### Repository structure
- `_whatsnew/` – Date-stamped include files consumed by `whats-new.adoc` for What's new entries.
- `_include/` – Reserved include directory for shared, reusable AsciiDoc snippets. It's currently a placeholder directory.
- `media/` – Image asset directory for screenshots used in alert list, filtering, and alert detail topics.

### Product-specific context

**Key concepts:**
- *Alerts* are storage issues or potential risks grouped by *severity* and *impact area*; documented severities are *Critical*, *Warning*, and *Informational*.
- *Impact areas* are *Capacity*, *Performance*, *Protection*, *Availability*, *Security*, and *Configuration*.
- Alert sources are a combination of selected *EMS* events and *metric-based* alerts.
- The NetApp Console *Notifications* feature is separate from ONTAP alerts and should not be treated as the same UI or data set.
- Access is organization-scoped: users must belong to the NetApp Console organization, and visible alerts depend on access to the underlying cluster resource.

**Naming conventions and terminology:**

- *Console agent* - connectivity component that links NetApp Console to on-premises ONTAP environments.
- *ONTAP System Manager* - the management interface for drilling into cluster and alert details.
- *EMS* - An acronym for vent message system that is used to send alerts about ONTAP. 

### Typical user workflows

- *Access and setup* - Access the Console, check connectivity to the Console agent, and discover ONTAP systems in the NetApp Console.
- *Review alerts* - View ONTAP alerts (both EMS and non-EMS alerts) to stay informed about risks or potential risk in ONTAP storage system. Learn information about an alert and the cluster that generated the alert. 
