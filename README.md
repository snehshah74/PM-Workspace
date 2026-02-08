# Product Manager Workspace

A structured workspace for Product Managers to create, manage, and maintain product documentation, track work in Jira, and publish to Confluence following consistent standards and workflows.

## 📁 Workspace Structure

```
Sneh PM-workspace/
├── .cursorrules          # AI assistant rules for PM workflows
├── README.md            # This file
├── artifacts/           # Temporary files, drafts, and working documents
├── docs/
│   ├── prds/           # Product Requirements Documents
│   ├── status-reports/ # Weekly and monthly status reports
│   └── templates/      # Reusable document templates
```

## 🚀 Quick Start

1. **Familiarize yourself with the rules**: Read the `.cursorrules` file to understand the workflow standards
2. **Create your first PRD**: Use the PRD structure in `.cursorrules` as a guide
3. **Set up Jira tickets**: Always create epics first, then link stories/tasks to them
4. **Start status reports**: Create your first weekly status report in `docs/status-reports/`

## 📋 How to Use This Workspace

### Using the .cursorrules File

The `.cursorrules` file contains standardized workflows that your AI assistant (Cursor) will follow when helping you with PM tasks. When you ask the AI to:
- Create a PRD → It will use the standard PRD structure
- Draft a Jira ticket → It will ensure epic linking and use the template
- Write a status report → It will follow the weekly status report format
- Help with Confluence → It will guide you through the publishing workflow

**Tip**: Reference the `.cursorrules` file when creating documents to ensure consistency.

### Creating a PRD (Product Requirements Document)

1. **Navigate to the PRD directory**:
   ```bash
   cd docs/prds/
   ```

2. **Create a new PRD file** following the naming convention:
   - Format: `PRD-[Feature-Name]-[YYYY-MM-DD].md`
   - Example: `PRD-User-Authentication-2024-01-15.md`

3. **Use the standard PRD structure** (from `.cursorrules`):
   - Header Section (Title, Version, Status)
   - Executive Summary
   - Problem Statement
   - User Stories & Requirements
   - Technical Considerations
   - Design & UX
   - Success Metrics
   - Timeline & Milestones
   - Risks & Mitigation
   - Appendices

4. **Link related documents**:
   - Add links to Jira epics/tickets
   - Reference Confluence pages
   - Include design file links (Figma, etc.)

**Example PRD creation workflow**:
```
1. Ask AI: "Create a PRD for [feature name]"
2. AI generates PRD following the standard structure
3. Review and customize the content
4. Save to docs/prds/
5. Create corresponding Jira epic
6. Link PRD to epic
```

### Creating Jira Tickets

#### Step 1: Create the Epic First
- **Epic Name Format**: `[Feature Area] - [Brief Description]`
- **Epic Description Must Include**:
  - Business value
  - Success metrics
  - High-level scope
  - Timeline estimate

#### Step 2: Create Stories/Tasks
- **Always link to parent epic** using the "Epic Link" field
- **Use the ticket description template**:
  ```markdown
  ## Overview
  [Brief description]

  ## Acceptance Criteria
  - [ ] Criterion 1
  - [ ] Criterion 2

  ## User Story
  As a [user type], I want [goal], so that [benefit]

  ## Related Links
  - PRD: [link]
  - Epic: [link]
  ```

#### Step 3: Complete Mandatory Fields
- ✅ Summary (max 60 characters)
- ✅ Priority (Blocker, Critical, High, Medium, Low)
- ✅ Labels (e.g., `frontend`, `backend`, `api`)
- ✅ Components
- ✅ Sprint assignment
- ✅ Epic Link (MANDATORY)

**Jira Workflow Checklist**:
- [ ] Epic created
- [ ] Story/Task created
- [ ] Epic Link field set
- [ ] Description template filled
- [ ] Labels and components added
- [ ] PRD linked (if applicable)
- [ ] Watchers added (stakeholders, engineers)

### Creating Status Reports

1. **Navigate to status reports directory**:
   ```bash
   cd docs/status-reports/
   ```

2. **Create a new status report**:
   - File name: `Status-Report-[YYYY-MM-DD].md`
   - Example: `Status-Report-2024-01-19.md`

3. **Follow the standard structure**:
   - Executive Summary (with Green/Yellow/Red status)
   - This Week's Accomplishments
   - In Progress
   - Next Week's Priorities
   - Metrics & KPIs
   - Risks & Blockers
   - Stakeholder Updates

4. **Use formatting guidelines**:
   - Include traffic light indicators: 🟢 🟡 🔴
   - Link to Jira tickets: `[TICKET-123]`
   - Link to PRDs and Confluence pages
   - Use tables for metrics

5. **Timeline**: 
   - Create every Friday EOD
   - Send to stakeholders via email
   - Publish to Confluence within 24 hours

**Status Report Template Example**:
```markdown
# Status Report - Week of 2024-01-19

## Executive Summary
🟢 **Overall Status: Green**
- Feature X completed and deployed
- Sprint on track

## This Week's Accomplishments
- [TICKET-123] - Completed user authentication flow
- [TICKET-124] - Deployed to staging environment

## In Progress
- [TICKET-125] - Payment integration (Expected: Jan 26)
- [TICKET-126] - API documentation (Blocked: Waiting on design)

## Next Week's Priorities
- Complete payment integration
- Begin user testing phase
```

### Publishing to Confluence

#### Pre-Publishing Checklist
Before publishing any document to Confluence, ensure:
- [ ] Document reviewed and proofread
- [ ] All links verified and working
- [ ] Images/screenshots included and optimized
- [ ] Tags/labels added
- [ ] Page permissions set correctly
- [ ] Related pages linked
- [ ] Table of contents added (for long documents)

#### Publishing Workflow

1. **Draft Creation**
   - Create page in Confluence
   - Use appropriate template (PRD, Status Report, etc.)
   - Add content following structure guidelines

2. **Review Process**
   - Share draft link with reviewers
   - Collect feedback
   - Make revisions
   - Get approval (if required)

3. **Final Publishing**
   - Set page permissions (view/edit)
   - Add to relevant space navigation
   - Add watchers/notifications
   - Publish page

4. **Post-Publishing**
   - Share link with stakeholders
   - Add to index/landing pages
   - Update related pages with links
   - Archive old versions (if updating existing page)

#### Confluence Page Types

**PRD Pages**
- Space: Product/Product Requirements
- Labels: `prd`, `requirements`, `[feature-name]`
- Parent: Product Requirements Index

**Status Reports**
- Space: Product/Status Reports
- Labels: `status-report`, `weekly-update`, `[team-name]`
- Parent: Status Reports Archive

**Meeting Notes**
- Space: Product/Meetings
- Labels: `meeting-notes`, `[meeting-type]`, `[date]`
- Include: Attendees, Agenda, Decisions, Action Items

## 🔗 Document Linking Best Practices

Always maintain links between related documents:

```
PRD ↔ Jira Epic ↔ Jira Stories/Tasks ↔ Confluence Page
```

**Example linking workflow**:
1. Create PRD → Save to `docs/prds/`
2. Create Jira Epic → Link PRD in epic description
3. Create Jira Stories → Link to epic and PRD
4. Publish PRD to Confluence → Link Confluence page in PRD
5. Update all documents with cross-references

## 📝 File Naming Conventions

- **PRDs**: `PRD-[Feature-Name]-[YYYY-MM-DD].md`
- **Status Reports**: `Status-Report-[YYYY-MM-DD].md`
- **Templates**: `Template-[Document-Type].md`
- **Artifacts**: Use descriptive names with dates

## ✅ Quality Standards

- **Proofreading**: All documents must be proofread before publishing
- **Language**: Use clear, concise language
- **Visual Aids**: Include screenshots, diagrams, and mockups where helpful
- **Consistency**: Maintain consistency across all documents
- **Updates**: Keep documents up-to-date

## 🎯 Weekly Workflow Checklist

**Monday**:
- [ ] Review previous week's status report
- [ ] Plan week's priorities
- [ ] Update Jira tickets

**Throughout the Week**:
- [ ] Create/update PRDs as needed
- [ ] Create Jira tickets (always link to epics!)
- [ ] Update status report with progress

**Friday**:
- [ ] Complete weekly status report
- [ ] Send status report to stakeholders
- [ ] Publish status report to Confluence
- [ ] Archive completed documents

## 🛠️ Tips & Tricks

1. **Use AI Assistant**: Ask Cursor to help create documents following the `.cursorrules` standards
2. **Templates**: Create reusable templates in `docs/templates/` for common document types
3. **Version Control**: Use git to track changes to your documents
4. **Search**: Use consistent labels and tags for easy searching in Confluence
5. **Automation**: Set calendar reminders for status report deadlines

## 📚 Additional Resources

- **Jira**: [Your Jira instance URL]
- **Confluence**: [Your Confluence instance URL]
- **Design Files**: [Figma/Design tool URL]
- **Product Wiki**: [Internal wiki URL]

## 🤝 Contributing

If you're working with a team:
1. Follow the same file naming conventions
2. Use the `.cursorrules` standards
3. Link documents consistently
4. Keep the workspace organized

## 📞 Support

For questions or suggestions about this workspace:
- Review the `.cursorrules` file for detailed guidelines
- Check existing documents for examples
- Ask your AI assistant for help following the standards

---

**Last Updated**: 2024-01-19  
**Maintained by**: Product Team
