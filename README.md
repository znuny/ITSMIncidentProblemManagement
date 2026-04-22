<div align="center">
  <a href="https://www.znuny.org">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://www.znuny.com/assets/znuny-logo.svg">
      <img alt="Znuny" src="https://www.znuny.com/assets/znuny-logo-black.svg" width="300">
    </picture>
  </a>

  ![Build status](https://badge.proxy.znuny.com/ITSMIncidentProblemManagement/rel-7_3)
</div>

ITSM Incident and Problem Management
=====================================

**Feature List**

This package provides ITSM Incident and Problem Management for Znuny. It extends the ticket system with ITSM-specific types and states for incidents and problems.

- **Ticket Types**: Adds ITSM ticket types (Incident, Incident::Major, ServiceRequest, Problem) for classification
- **Ticket States**: Adds state "closed with workaround" for workaround-based closure
- **Additional ITSM Fields**: Agent screen for additional ITSM-related ticket fields (AgentTicketAddtlITSMField)
- **Decision Handling**: Agent screen for ticket-related decisions (AgentTicketDecision)
- **Service Incident State**: Agent ticket screens dynamically show the selected service’s incident state (traffic-light style indicator + translated text) via AJAX. Implemented as JSON-only backend action `AgentITSMIncidentProblemManagement` (`Subaction=GetServiceIncidentState`)—there is no separate “overview” screen to open from the menu; the action is used by the frontend. Enable per screen in SysConfig (`*ShowIncidentState`); ensure ACL allows this action if AJAX is blocked
- **Ticket Configuration**: ITSM ticket and type configuration (ITSMTicket.xml, TicketITSMTicket.xml) for integration with services and SLAs
- **Dynamic Statistics**: Backend for dynamic stats (e.g. first-level solution rate, solution time average) used by ITSM Service Level Management

**Prerequisites**

- Znuny 7.3
- ITSMCore 7.3.1

**Installation**

Install via Admin interface → Package Manager. The package is part of the Znuny ITSM stack and can be installed from the Znuny repository or from a built .opm file.

**Configuration**

Configuration is available in the System Configuration under ITSMIncidentProblemManagment. Relevant agent actions for ACLs include `AgentITSMIncidentProblemManagement`, `AgentTicketAddtlITSMField` and `AgentTicketDecision`.

**Download**

Source code is available in the [ITSMIncidentProblemManagement repository](https://github.com/znuny/ITSMIncidentProblemManagement). For packaged releases, use the Znuny package repository or build from source.

**Commercial Support**

For this extension and for Znuny in general visit [www.znuny.com](https://www.znuny.com). Looking forward to hear from you!

Enjoy!

Your Znuny Team!

[www.znuny.com](https://www.znuny.com)
