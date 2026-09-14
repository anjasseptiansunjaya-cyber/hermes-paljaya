# Hermes Paljaya

Hermes Paljaya is a personal automation assistant for construction-project
administration. The current website describes a single-user application that runs
on its owner's computer and works with data in that owner's Google account. It is
not a claim that Google OAuth verification has been completed or approved.

## Website deployment

The repository is a static site containing `index.html` and `privacy.html`.
Publish both files at stable HTTPS URLs on the production domain. Confirm that:

- the homepage loads without authentication;
- the homepage links to the privacy policy and developer contact;
- the privacy policy is reachable at its final public URL;
- all links work from the deployed origin; and
- the deployed text matches the scopes and behavior of the production code.

Replace every `[EMAIL PENGEMBANG — isi sebelum publikasi]` placeholder before
publishing. Use an active developer/privacy contact address and keep it consistent
with the Google Cloud OAuth consent-screen contact.

## OAuth consent-screen prerequisites

Before requesting review, the owner must confirm the production Google Cloud
project and OAuth client, then configure the consent screen with:

1. The exact application name, homepage URL, privacy-policy URL, and authorized
   domains used by the deployed site.
2. An active developer contact email and, where required by the project, a
   support email.
3. Only the scopes actually requested by the deployed code. The current policy
   documents these scope strings and their purposes:
   `https://www.googleapis.com/auth/spreadsheets`,
   `https://www.googleapis.com/auth/documents`,
   `https://www.googleapis.com/auth/drive`,
   `https://www.googleapis.com/auth/gmail.readonly`,
   `https://www.googleapis.com/auth/gmail.modify`,
   `https://www.googleapis.com/auth/gmail.send`,
   `https://www.googleapis.com/auth/calendar`, and
   `https://www.googleapis.com/auth/contacts.readonly`.
4. Test users, publishing status, redirect URIs, and authorized JavaScript
   origins that match the actual OAuth client configuration.

The owner must remove any documented scope that the production application does
not request, and must add and justify any scope that it does request. Gmail and
other sensitive or restricted scopes may require additional review, security
assessment, or a different verification path under Google's current rules.

## Evidence and reviewer walkthrough

Provide evidence from the production configuration rather than screenshots of
unreleased behavior:

- the deployed homepage and privacy-policy URLs;
- a scope list exported from the OAuth consent-screen configuration and matching
  the scope-by-scope table in `privacy.html`;
- a short screen recording or screenshots showing the OAuth consent flow and the
  product behavior for each requested scope;
- a test account or reviewer instructions that do not expose unrelated private
  information;
- a description of where tokens and temporary results are stored and how the
  owner deletes them; and
- a clear demonstration of Google Account access revocation at
  <https://myaccount.google.com/permissions>.

The current pages describe local processing and no public user registration
because that is the behavior represented by the repository content. Do not submit
claims about multi-user support, server-side storage, sharing, automated email
delivery, or other features unless the deployed code and documentation support
them. The Limited Use commitments in `privacy.html` must remain true for the
production implementation and any service used with it.

## Owner information still required

Before submission, obtain and record:

- the real developer/privacy email address;
- production homepage and privacy-policy URLs;
- Google Cloud project ID, OAuth client ID, publishing status, redirect URIs,
  and authorized domains;
- the final production scope list; and
- a reviewer-safe demo video or equivalent evidence covering the requested scopes.

Google controls the verification decision. Completing this checklist improves
readiness but cannot guarantee approval.
