---
name: Angellist
description: Use when helping fund managers and investors manage fundraising workflows, including creating and sharing data rooms, managing digital subscription documents, inviting investors, tracking analytics, and handling investor onboarding and document collection.
metadata:
    mintlify-proj: angellist
    version: "1.0"
---

# AngelList Investor Management Platform

## Product summary

AngelList Investor Management Platform is a suite of tools for fund managers to centralize investor prospecting, closing, and communication workflows. The platform includes three core products: **Data Room** (branded document sharing), **Digital Subscriptions** (investor onboarding and paperwork automation), and **Investor Portal** (investor profile and document management). Agents use this skill to help users create data rooms, manage subscription templates and transactions, invite investors, configure permissions, track analytics, and handle bulk operations. Primary documentation: https://support.angellist.com. Key entry point: https://portal.angellist.com. Contact support at portal@angellist.com.

## When to use

Reach for this skill when:
- A user needs to create or configure a Data Room for investor access
- A user is setting up Digital Subscriptions templates or inviting investors to fill out documents
- A user needs to manage investor access, permissions, or bulk invite workflows
- A user is troubleshooting transaction statuses, revisions, or document uploads
- A user needs to configure call-to-action buttons, analytics, or integrations
- A user is managing the Investor Portal, vehicles, or bulk document uploads
- A user encounters access errors, permission issues, or account problems

## Quick reference

### Core Products & Entry Points

| Product | Purpose | Primary URL |
|---------|---------|------------|
| Data Room | Branded document sharing for investors | portal.angellist.com → Data Room tab |
| Digital Subscriptions | Investor onboarding & paperwork automation | portal.angellist.com → Digital Subscriptions tab |
| Investor Portal | Investor profiles, vehicles, directory management | portal.angellist.com → Investor Portal tab |

### Transaction Statuses (Digital Subscriptions)

| Status | Meaning | Action |
|--------|---------|--------|
| Created | Investor started via public link, no data entered | Waiting for investor input |
| Invited | Private email invite sent, not yet started | Resend if needed (one-click only) |
| Pending Investor | Investor filling out form, not complete | Waiting for investor |
| Submitted | All info filled & signed, not yet reviewed | Review and request revisions or approve |
| Pending Review | Fund manager reviewing submission | Request revisions or mark "In Good Order" |
| Pending Revision | Investor requested to fix/clarify info | Waiting for investor resubmission |
| In Good Order | Fund manager approved submission | Ready for counter-signature if needed |
| Confirmed | Fund manager accepted, process complete | Final status (may include counter-signature) |

### Data Room Access Levels

| Access Level | Verification | Analytics | NDA Enforcement |
|--------------|--------------|-----------|-----------------|
| Verified email | Email verification or AngelList login | User-level | Auto-enforced |
| Password only | Password (system-generated) | Anonymous link-level | Not enforced |
| Unverified email | Any email address | Email-level | Toggle on/off |
| Public access | None | Anonymous link-level | Not enforced |

### Permission Groups & Viewer Permissions

- **View Only**: Investors can view documents but not download
- **View & Download**: Investors can view and download documents
- **Custom Access**: Restrict to specific folders/documents per investor group

### Data Room Section Types

Text, Featured Documents, Team, Video, FAQs, Co-Investors, All Documents (default)

## Decision guidance

### When to use Public Link vs Private Email Invite (Transactions)

| Scenario | Use Public Link | Use Private Email Invite |
|----------|-----------------|-------------------------|
| Open call to multiple investors | ✓ | |
| Specific investor, trackable | | ✓ |
| One-time security concern | | ✓ (one-click only) |
| Bulk investor outreach | | ✓ (send multiple) |
| Resending to same investor | ✓ (link stays active) | ✗ (must create new) |

### When to use Email Invite vs Public Access Link (Data Room)

| Scenario | Email Invite | Public Link |
|----------|--------------|------------|
| Specific investor group | ✓ | |
| Track individual views | ✓ | |
| Open fundraising | | ✓ |
| Require verification | ✓ (verified email) | ✓ (varies by setting) |
| Anonymous tracking acceptable | | ✓ |

### When to use Bulk Upload vs Individual Upload

| Task | Bulk Upload | Individual |
|------|------------|-----------|
| 1-2 files | | ✓ |
| 10+ files to multiple investors | ✓ | |
| K-1s, capital calls, reports | ✓ | |
| Single file to all investors in fund | Use Vehicle Files tab | |

## Workflow

### Create and Launch a Data Room

1. **Navigate to Data Room tab** in portal.angellist.com
2. **Click "Create Data Room"** and name it
3. **Configure page layout**: Add sections (text, documents, team, video, FAQs, co-investors)
4. **Upload documents**: Go to Documents tab, upload files, organize into folders
5. **Set up access**: Go to Access tab, create permission groups (View Only, View & Download, Custom)
6. **Configure CTAs**: Add call-to-action buttons (Digital Subscriptions templates, website links, or email)
7. **Invite investors**: Use email invites for specific investors or create public access links
8. **Publish**: Save all settings and share access links or send invites
9. **Monitor**: Track analytics in Activity tab to see views, downloads, time spent

### Invite Investors to Fill Out a Transaction (Digital Subscriptions)

1. **Go to Digital Subscriptions → Transactions tab**
2. **Choose method**:
   - **Public Link**: Click Template → Copy Link → Share URL
   - **Private Email**: Click "New Transaction" → Fill sender entity, template, recipient name/email → Create
3. **For private email**: System sends one-click invite from portal-notifications@angellist.com
4. **Track status**: Monitor transaction status as investor progresses
5. **Review submission**: When status = "Submitted", open transaction and review
6. **Request revisions** (if needed): Click specific fields → Request revision → Investor resubmits
7. **Finalize**: Click "Finalize" → Select "In Good Order" or "Rejected"
8. **Counter-sign** (if required): Authorized signatories receive email to sign

### Bulk Upload Documents to Investor Profiles

1. **Go to Investor Portal → Directory → Bulk Uploads**
2. **Download mapping template** with Directory Entity and Vehicle IDs
3. **Prepare files**: Rename each file with format: `eId=<ID>~vehicleId=<ID>~fileName=<name>~fileCategory=<category>~customerId=<ID>`
4. **Create ZIP file** with all renamed documents
5. **Upload ZIP** through interface
6. **Review validation results**: System flags naming/mapping errors
7. **Remove errored files** (optional) and proceed with valid files
8. **Send notifications** (optional): Customize email copy to notify investors
9. **Confirm**: Finish upload

### Manage Transaction Revisions

1. **Open submitted transaction** (status = "Submitted" or "Pending Review")
2. **Review investor data** for errors, missing info, or unclear documents
3. **Request revision**: Click specific field → Add revision request with instructions
4. **Request additional documentation**: Add new field for investor to complete
5. **Send back**: Investor receives notification and can edit without restarting
6. **Investor resubmits**: Status returns to "Pending Review"
7. **Finalize when satisfied**: Click "Finalize" → "In Good Order" or "Rejected"

## Common gotchas

- **One-click email invites expire**: Private email invites are one-click only for security. After investor clicks, link becomes null. Must create new transaction to resend.
- **Templates must be associated with Vehicles**: If Digital Subscriptions CTAs don't appear in Data Room, verify the Vehicle holding the template is connected in Settings tab and template's public link is enabled.
- **Invite expiration**: Email invitations expire after 75 days and cannot be refreshed. User must request new invite from sender.
- **Cannot manually change transaction status**: Status changes only based on investor actions. Contact portal@angellist.com if status appears stuck.
- **Cannot delete transactions**: Only AngelList team can delete. Guardrails prevent accidental deletion.
- **Bulk upload file naming is strict**: Files must follow exact naming convention or validation fails. Download template and follow format precisely.
- **Server errors**: If receiving "Server Error" or "You are not a part of an organization", clear cache/cookies and reset URL to https://portal.angellist.com. If persists, email portal@angellist.com.
- **Wrong account for invite**: "You are not a part of an organization" error often means user accepted invite on different email than signed-in account. Verify email matches.
- **Authorized signatory mismatch**: If user cannot sign transaction, their account role may not be set as authorized signatory. Contact portal@angellist.com to upgrade role.
- **Vehicle creation**: Vehicles (funds/SPVs) cannot be created by users—only AngelList team creates them. Request new vehicle at portal@angellist.com.
- **Sub-level vehicles not supported**: Master-feeder structures should be set up as separate vehicles (onshore, offshore, tax-exempt) not nested.
- **Bulk upload to all investors**: Don't use Bulk Upload tool for single file to all investors in fund. Instead, upload directly to Vehicle's Files tab.

## Verification checklist

Before submitting work with AngelList Investor Management Platform:

- [ ] **Data Room**: Verify all documents uploaded, folders organized, permission groups configured, CTAs set up, and access links created/tested
- [ ] **Transactions**: Confirm template selected, recipient email correct, sender entity specified, and transaction created successfully
- [ ] **Invites**: Verify email addresses are correct, permission groups assigned, and invites sent from correct sender entity
- [ ] **Permissions**: Confirm permission groups match investor access needs (View Only vs View & Download vs Custom)
- [ ] **CTAs**: Test that call-to-action buttons link to correct templates, websites, or email addresses
- [ ] **Bulk operations**: Validate file naming follows template format, ZIP structure correct, and validation passed before confirming
- [ ] **Transaction review**: Check all investor data is complete, documents legible, and revisions (if any) have been addressed
- [ ] **Analytics**: Confirm Activity tab shows expected visitor activity and file access patterns
- [ ] **Status tracking**: Verify transaction status matches expected stage and no errors appear in dashboard
- [ ] **Account access**: Confirm user has correct role (admin, view/edit, manage team members) and authorized signatory status if needed

## Resources

**Comprehensive navigation**: https://support.angellist.com/llms.txt

**Critical documentation pages**:
- Data Room Overview: https://support.angellist.com/data-room/overview/what-is-data-room
- Digital Subscriptions Transactions: https://support.angellist.com/digitalsubs/transactions/transactions-overview
- Investor Portal Vehicles & Directory: https://support.angellist.com/portal/general/vehicles

**Support**: Email portal@angellist.com for account issues, new vehicle creation, API setup, or template requests.

---

> For additional documentation and navigation, see: https://support.angellist.com/llms.txt