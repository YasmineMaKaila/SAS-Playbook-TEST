# SAS Pod Playbook

## Purpose

An interactive quick-reference resource for Screening and Applications (SAS)
associates who temporarily move to another pod, permanently transfer between
pods, are promoted into a role requiring knowledge of additional pods, or need
a rapid refresher while supporting another region.

This is a **performance-support resource** — it supplements, and does not
replace, the SAS Standard Workflow Manual or formal SAS training.

## Files included

```
sas-pod-playbook/
├── index.html      # The complete, self-contained application
└── README.md       # This file
```

`index.html` is fully self-contained: all visual assets (Cortland logo, LXD
mark, illustration) are embedded directly in the file as inline images.
Nothing else needs to be uploaded for the site to work. The only external
requests the page makes are to Google Fonts (for the Poppins/Inter typefaces);
if that request is blocked in a given network, the page still functions
normally using the browser's fallback fonts.

## Publishing to GitHub Pages

1. Create a new GitHub repository (or use an existing one).
2. Add `index.html` to the root of the repository (or to a `/docs` folder —
   either works with GitHub Pages).
3. In the repository, go to **Settings → Pages**.
4. Under **Source**, select the branch and folder containing `index.html`.
5. Save. GitHub will publish the site at
   `https://<your-org-or-username>.github.io/<repository-name>/`.

The page uses only relative behavior and embedded assets — no absolute
(root-relative) paths — so it works correctly whether it's served from the
root of a `username.github.io` site or from a project subdirectory like
`username.github.io/sas-pod-playbook/`.

No build step, backend, server, or database is required. It is a static
HTML file.

## Source of truth

**The approved `SAS Playbook Info 2026.docx` Word document remains the sole
authoritative source for all SAS pod operational content.** This website is
a presentation and performance-support layer built from that document — it
is never the authority for policy itself. If the interface and the Word
document ever appear to disagree, the Word document governs, and the
discrepancy should be reported rather than resolved by editing the site.

A companion **content reconciliation report** and **SME/Talent review-flag
report** were produced alongside this build. They document exactly how every
piece of the Word document was classified into this site's General Pod
Information / Property-Specific Information structure, and list every item
of source wording that appeared ambiguous, inconsistent, or incomplete and
was preserved as-is pending subject-matter-expert review rather than
corrected unilaterally. Neither report is included in this deployment
package, since they're internal governance documents, not part of the public
site.

## Updating pod content after the source document changes

This site has no content-management system or database — the operational
content for each pod lives directly inside `index.html`, in a JavaScript data
structure near the top of the file's `<script>` section (look for
`const PODS = [ ... ]`). Each pod is one object in that array with:

- `sections` — General Pod Information: policy that applies across the whole
  pod (fees, deposits, pet policies, concessions, screening rules, etc.).
- `propertyExceptions` — Property-Specific Information: unusual details that
  apply to one named community only, and should never also appear in
  `sections` for the same fact.
- `meta.sourceRefreshedDate` — the date this pod's data was last synchronized
  from the approved Word document.
- `meta.humanVerifiedDate` / `meta.verifiedBy` — left blank until a SAS SME
  or department lead has actually reviewed and signed off on the content.
  Refreshing the source is not the same as verifying it — these two dates
  are intentionally kept separate and neither should be set automatically.

To update a pod after the Word document changes:

1. Re-read the relevant section of the approved Word document.
2. Edit that pod's `sections` / `propertyExceptions` arrays to match,
   preserving the source's exact wording and figures (this tool does not
   rewrite or "clean up" operational language — only reorganizes it
   visually).
3. Update `meta.sourceRefreshedDate` to the date of the refresh.
4. Leave `meta.humanVerifiedDate` and `verifiedBy` untouched unless an
   authorized reviewer has actually signed off on the updated content.
5. If anything in the source is unclear, inconsistent, or incomplete,
   preserve it as written and add an entry to that pod's `reviewFlags` array
   rather than guessing at a correction. `reviewFlags` are never shown to
   associates — they exist for governance and the SME review process only.

No pod's content should ever be added, removed, or reworded from any source
other than the approved Word document.

## Version

Version 1 — all 11 SAS pods (GA Pod 1, NC Pod 3, North FL Pod 4, South FL Pod
6, OH/TN Pod 7, Pod 8 VA, Pod 9 North Dallas, CFW Pod 10, HASA Pod 11, Pod 12
Mountain West, Pod 13: AZ). Built September 2026.
