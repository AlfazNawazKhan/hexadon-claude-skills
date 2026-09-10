---
name: notion-mastery
description: Build, structure, and automate Notion 3.0 workspaces covering Docs, Projects, Sprints, Databases, Notion Calendar, Notion Mail, Forms, Notion Sites, and AI Agents. Use this skill whenever the user asks to create, organize, or optimize a Notion workspace, set up databases, relations, rollups, formulas, dashboards, AI agents, habit trackers, or publish Notion sites—even if they only mention general productivity, task management, or note-taking.
---

# Notion 3.0 Workspace Architecture & Automation Skill

Follow this workflow to architect, construct, and automate full-featured Notion 3.0 workspaces across its six core pillars: Docs, Projects, Calendar, Sites, Mail, and AI.

---

## 1. Workspace Hierarchy & Settings Setup
1. **Workspace & Teamspace Architecture**:
   - Organize content into top-level containers: Workspaces > Teamspaces > Pages > Subpages/Databases.
   - Configure user roles according to strict permissions:
     - **Owner/Admin**: Full workspace access, billing, and global settings management.
     - **Member**: Employees with workspace-wide access (paid tier).
     - **Guest**: External collaborators restricted to specifically shared pages (free up to plan limit).
   - Set granular page permission levels: `Full access`, `Can edit`, `Can comment`, `Can view`.
2. **Preference Configurations**:
   - Set week start to Monday for calendar consistency.
   - Configure notification channels (desktop, mobile, email, Slack/Discord).
   - Set trusted domain access to restrict workspace membership by email domain.

---

## 2. Block Formatting & Dashboard Construction
1. **Block Mechanics & Slash Commands**:
   - Execute block creation via forward-slash commands (`/text`, `/h1`, `/todo`, `/bullet`, `/image`, `/column`, `/divider`).
   - Use block handles (6 dots) to drag, create multi-column layouts, or transform blocks (`Turn into`).
   - Construct **Synced Blocks** (`/sync`) for universal content updates across multiple pages.
2. **Home Dashboard Architecture**:
   - Build a 2-column daily dashboard layout:
     - **Left Column (Life/Personal)**: Links to Tasks, Journal, Habits, and quick action buttons (`/button`).
     - **Right Column (Work/Team)**: Links to Active Projects, Team Calendar, SOPs, and Meeting Notes.
   - Embed dynamic linked views (`/linked view of data source`) filtered specifically to `Assignee = Me`.

---

## 3. Database System Architecture (Basic to Advanced)
1. **Database Views & Properties**:
   - Support 10 database layouts: Table, Board (Kanban), Timeline, Calendar, List, Gallery, Chart, Feed, Map.
   - Core Properties: `Title`, `Select`, `Multi-select`, `Date`, `Person`, `URL`, `Files & media`, `Checkbox`.
   - Remember: Every row in a Notion database functions as a full-featured nested subpage.
2. **Advanced Relations & Aggregations**:
   - **Relations**: Connect two databases using two-way relation properties (e.g., linking Tasks to Projects).
   - **Rollups**: Aggregate data across relations (e.g., counting tasks where `Status = Not Started` or displaying overall progress percentage).
   - **Formulas**: Write custom calculations using properties and conditionals, or prompt Notion AI to write syntax for dynamic status icons and due date calculations.

---

## 4. Notion Projects & Sprint Management
1. **Official Projects & Tasks Setup**:
   - Deploy the native **Projects & Tasks** structure with two interconnected databases.
   - Enable **Sprints** via database settings on the Tasks database.
2. **Sprint Board Workflow**:
   - Maintain three primary views:
     - **Current Sprint**: Grouped by status, showing active sprint items.
     - **Sprint Planning**: Board for dragging backlog tasks into upcoming sprint cycles.
     - **Backlog**: Master list of unassigned tasks.
   - Complete sprints using automatic rollover: incomplete tasks automatically push to the next active sprint.

---

## 5. Notion Calendar & Scheduling Integration
1. **External Integration**:
   - Connect Google or Apple Calendars to sync meetings alongside database tasks.
2. **Scheduling Links & Conflict Avoidance**:
   - Generate recurring or one-off availability booking links directly from Notion Calendar.
   - Utilize multi-calendar coordination to automatically prevent double-booking across personal and work accounts.
   - Map database date fields to calendar views to enable drag-and-drop rescheduling.

---

## 6. Notion Mail & Smart Workflows
1. **Inbox Management**:
   - Group emails flexibly by property (Sender, Date, Importance, Custom Select Status).
2. **AI Drafting & Auto-Labeling**:
   - Use AI writing assistants within the compose window, referencing Notion pages using `@page-name`.
   - Create automated AI rules to scan incoming mail and auto-apply labels (e.g., label emails from `@company.com` as `Internal`).
   - Track team inbox workflows using custom select properties (`Needs Reply`, `Waiting`, `Done`).

---

## 7. Forms, Data Capture & Knowledge Hubs
1. **Native Database Forms**:
   - Convert any database into a public or workspace-restricted web form (`/form`).
   - Configure question requirements, help text, long-form fields, and response triggers.
2. **Automations on Submission**:
   - Set up database triggers (`When page added`) to execute actions automatically (e.g., sending email notifications).
3. **Clippings & Knowledge Base**:
   - Construct a `Knowledge` database with properties: `Type` (Note/Clipping), `URL`, `Authors`, `Date`, and `Content`.
   - Capture web pages using the Notion Web Clipper extension for seamless reference by Notion AI.

---

## 8. Journaling & Habit Tracking Systems
1. **Automated Journaling**:
   - Create a `Journal` database with a `Daily Reflection` template containing structured reflection prompts.
   - Configure the template to auto-repeat daily at a specified end-of-day time.
2. **Habit Tracker Integration**:
   - Set up a `Habits` database with multi-select fields for daily habit tracking.
   - Add a quick-action button in the Journal template to automatically generate today's habit tracking row.
   - Visualize progress over time using chart views grouped by date/month.

---

## 9. Notion Sites, Publishing & Wikis
1. **Site Publishing & SEO**:
   - Turn any page into a web page via `Share > Publish`.
   - Configure SEO settings: search engine indexing toggle, custom page titles, meta descriptions, and social preview images.
   - Customize site themes, favicons, header navigation, and Google Analytics measurement IDs.
2. **Wikis & Verification**:
   - Convert knowledge base pages into official **Wikis** (`Turn into wiki`).
   - Enable verification settings (`Verify indefinitely` or set expiration durations) and lock pages to preserve official documentation integrity.

---

## 10. Notion AI & Autonomous Agents
1. **Q&A & Meeting Notes**:
   - Use workspace Q&A to query documentation and database statuses with restricted permission awareness.
   - Deploy AI Meeting Notes (`/ai meeting notes`) to transcribe, summarize, and generate action items directly into task databases.
2. **Custom AI Agents**:
   - Configure personal AI Agents with defined **Agent Identity**, **Chat Interaction Rules**, and **Memories**.
   - Direct agents to run multi-step autonomous tasks (up to 20 minutes) including web research, script drafting, database population, and subpage generation.

---

## 11. External Integrations & Capstone Architecture
1. **Third-Party Ecosystem**:
   - Connect external triggers and actions via Zapier (e.g., sending Gmail or Slack alerts on database updates).
   - Embed external content directly (`/embed`, Twitter/X posts, Figma, Loom, Google Docs) or add widgets from community libraries.
2. **Teamspace Capstone Standard**:
   - When building a complete team workspace, integrate:
     - Private Teamspace with Home Dashboard.
     - Connected Projects, Tasks, and Sprint databases.
     - Dedicated Meeting Notes database with AI transcription.
     - Client update automations linked to Notion Mail.
     - Verified Wiki Knowledge Base.
