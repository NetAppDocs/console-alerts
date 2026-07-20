## Copilot instructions for ONTAP alerts documentation

### Repository overview
Product: ONTAP alerts

ONTAP alerts is a NetApp Console service for viewing issues and potential risks in ONTAP storage environments. It surfaces selected EMS and metric-based alerts for ONTAP clusters and links alert and cluster details to ONTAP System Manager.

### Repository structure
- `./` – Main documentation topics and site configuration for ONTAP alerts, including concepts, prerequisites, setup, access, usage, FAQ, release notes entry page, and `project.yml` / `_index.yml`.
- `_whatsnew/` – Date-stamped include files consumed by `whats-new.adoc` for What's new entries.
- `_include/` – Reserved include directory for shared AsciiDoc snippets; currently empty except for a placeholder README.
- `media/` – Image asset directory for screenshots used in alert list, filtering, and alert detail topics.

### Product-specific context
**Architecture and components:**
- *ONTAP alerts* is a core component of *NetApp Console* and is accessed from *Storage* > *Alerts* in the Console UI.
- The service monitors *ONTAP clusters* and receives alert data from ONTAP; users view alerts in NetApp Console and can drill into related cluster details in *ONTAP System Manager*.
- A *Console agent* is required for on-premises regions so NetApp Console can connect to discovered ONTAP systems; alerts remain associated with the originating cluster and agent.
- This repository documents the *SaaS* NetApp Console experience only; ONTAP alerts is not available in a local Console agent UI or in direct mode.
- Supported platform pattern: on-premises *ONTAP NAS or SAN* systems in the same NetApp Console organization as an active Console agent; *Cloud Volumes ONTAP* is not supported.

**Key concepts:**
- *Alerts* in this product are storage issues or potential risks grouped by *severity* and *impact area*; documented severities are *Critical*, *Warning*, and *Informational*.
- *Impact areas* are *Capacity*, *Performance*, *Protection*, *Availability*, *Security*, and *Configuration*.
- Alert sources are a combination of selected *EMS* events and *metric-based* alerts.
- The NetApp Console *Notifications* feature is separate from ONTAP alerts and should not be treated as the same UI or data set.
- Access is organization-scoped: users must belong to the NetApp Console organization, and visible alerts depend on access to the underlying cluster resource.

**Naming conventions and terminology:**
- Use *NetApp Console* as the current platform name; older repository content and links may still use *BlueXP*.
- Use *ONTAP alerts* as the current product name; older release-note content may still refer to *BlueXP alerts*.
- *Console agent* is the connectivity component that links NetApp Console to on-premises ONTAP environments.
- *ONTAP System Manager* is the linked management interface for drilling into cluster and alert details.
- *EMS* means ONTAP event messages and is used as one alert source in this service.

### Typical user workflows
**Initial access and setup:** Review prerequisites → Ensure ONTAP systems are discovered in NetApp Console → Create or use a Console agent with ONTAP alerts capabilities → Wait for initial discovery → Open *Storage* > *Alerts*

**Review alerts:** Log in to NetApp Console → Open *Storage* > *Alerts* → Sort or filter the Alerts list page → Download CSV or select an alert → Review alert details and suggested corrective actions

**Drill into cluster details:** Open an alert from the Alerts list page → Select the cluster name → Open the linked cluster view in *ONTAP System Manager* → Review cluster information there
