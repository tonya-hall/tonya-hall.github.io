# Olea Development Plan (ODP)

## Overview
This is a plan to manage the product life cycle activities associated with Olea engineering. This encompasses design, meeting cadence, estimation, milestones, and deployment. Further, it defines the interactions between various teams.

### Current Issues:
- Poor clarity into future deliverables
- Poor clarity into deliverable status
- Too many meetings with disparate groups

## Assumptions
There are many, and they can (and will) be reversed based on team feedback.

## Communication
We use Slack to communicate as a development team.

- All of the company will be subscribed to `#general`.
- All of development will be in `#engineering`.
- Teams may separate as they see fit for smaller communications, but be sure to address the appropriate audience or link the conversation appropriately.

## Project Organization

| **Role**         | **Responsibility**                                                              |
|------------------|--------------------------------------------------------------------------------|
| Developers       | Execute tasks/stories                                                          |
| Scrummaster      | Responsible for resources, schedules, stakeholder management, and concerns      |
| Technical Lead   | The person with the most expertise                                              |
| Product Owner    | Visionary of the final product, liaison between stakeholders and Scrummaster     |
| Stakeholder      | Customers, C-Suite, Dependents, Analysts                                        |

## Development

### Development Methodology
Agile is not without its drawbacks, namely difficulty in long-term planning. However, it has a long track record in software development with many tools to help the process, including Jira. Many of the choices here are somewhat arbitrary but based on historical use. As per the assumptions, the team shall change this as needed.

[Introduction to Agile Methodology](https://www.youtube.com/watch?v=502ILHjX9EE)

### Work Management
Work will be managed on a common board for all development tasks.

#### Story/Ticket
- **Subject (high level)**
- **AC (Acceptance Criteria)**: User Story (I, person, want this so I can do that). Expected unit tests. Deliverables.
- Estimate in days. Week-long stories should be broken down at next planning.

Stories should be labeled as:
- Edge
- AI
- Swe
- Analytics

If a new ticket is created and will be worked on during the current sprint, it should be described in `#engineering`.

#### Epic
A collection of related Tickets that capture a larger-duration effort. Epic should have an estimated end date.

### Meeting Schedule
- **Virtual Standup**: Every day
- **Sprint Planning**: Every two weeks, Thursday morning before sprint end
- **Sprint Restart**: Every two weeks, Friday of sprint end
- **System Design**: On-demand

#### Virtual Standup
YTBW: Yesterday, Today, Blockers (optional), Work Location. No two days' status should ever be the same. Status should be complete by 9am CT and posted in `#olea_standup`.

**Example**:

y ODS-144 Finished Unit Test

t ODS-149 Began research in flugenheimer, began design doc

b Dr. Appt at 1, need help from finding flugenheimer spec sheet

w office till noon, home after dr. appt


### Sprint Planning
Review all upcoming milestones, estimate unplanned tickets, and verify prioritization and utilization for upcoming sprints. The meeting outcomes are:
- Updated estimate of completion and "on track" measure of active Epics.
- Detailed plan for three future sprints.
- Less-detailed plan for the upcoming calendar quarter.
- High-level technical roadmap for the upcoming year(s).

### Sprint Restart
Sprint Close: Verify closed tickets, demonstrate completion, and review any changes to this document. The Product Owner should perform backlog refinement before this meeting.

## Pirate Scrum Values (This will be deleted, but I wanted to address it once)

The following values should be held by team members in Scrum:
- **Accountability**: Be on time, own tickets, define "done."
- **Responsiveness**: Be available, focus on meetings.
- **Respectfulness**: Value others and their time.
- **Goal-Orientedness**: Align with business needs and ensure releasable completed tickets.
- **Transparency**: Overdocument and update status regularly.

## Design & Requirements

### Detailed Product Development Design Activities
- **Stakeholder Requirements Definition**: Expected validation steps and operational assumptions.
- **Stakeholder Requirements Review**: After review and revision, stakeholders sign the document.
- **System Requirements Definition**: Expected verification steps, interfaces, and performance measures.
- **System Requirements Review**: Technical leads and stakeholders review the document and sign after revisions.

### Design Definition
- **C4 Design Document**
- **Interface Descriptions**
- **Design Choices and Trade Studies**
- **Verification and Validation Approaches**

### Implementation

#### Verification
Does the implementation meet the design? Includes unit tests.

#### Validation
Did the product meet the requirements?

### Product Requirements
- Well-written
- Documented in a known location

### Software & Documentation Standards
Documentation should live in the same repository as the project it describes.

#### Software Standards
- **C software**: C11 standard
- **C++ software**: C++17 standard, Google C++ Style Guide
- **Python**: PEP8 standard
- **JavaScript**: ECMAScript 2015 standard, Google JavaScript Style Guide
- **Verification test reports**: GitLab JUnit XML format
- **Versioning**: Semantic Versioning 2.0.0
- **User manuals**: AsciiDoc 8.6.9 format

### Best Practices for Software, Design, and Documentation

#### Supabase Database Changes
- Use primary key as `tablename_id`, preferably a GUID.
- Include `created_at`, `updated_at`, `created_by`, `updated_by`.

#### Flutterflow New Pages
All new pages should be broadcast on `#engineering`. Be prepared to demonstrate during Sprint Close.

#### Version Control
Maintaining a tidy codebase is necessary for future maintenance and improvement.

**DO**:
- Use descriptive commit messages.
- Make atomic changes.
- Follow style and lint guidelines.

**DON’T**:
- Leave commented code in the codebase.

#### Copyright Notice
All source code, designs, and documentation must include the following at the head:

Copyright (c) 2024 Olea Edge Analytics, Inc. Distribution of this file or its parts, via any medium is strictly prohibited. Permission to use must be explicitly granted by Olea Edge Analytics, Inc.


#### VSCode Developer Docker
A common workspace housing all repositories and documentation, enforced through Docker, improves development consistency.

### Continuous Integration
All new code repositories will be built and linted nightly.
