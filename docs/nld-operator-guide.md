# Netherlands owner-sale operator guide

This runbook configures the governed 6810 actor for an owner selling
Dutch real estate. It is an evidence and workflow aid, not a notary,
broker, tax adviser or source of case-specific legal advice.

## Operating boundary

The actor may collect facts, build a checklist, detect missing evidence,
draft purchase-agreement inputs and assemble the notary package. It must
not sign an `akte van levering`, represent that title has passed, submit
an instrument to Kadaster, hold client money, or release proceeds. Those
actions belong to the parties and a Netherlands civil-law notary.

## Supervised workflow

1. Create a listing with jurisdiction `NLD`, the Kadaster parcel/address,
   every legal owner, buyer/seller party, price and occupancy status.
2. Obtain fresh Kadaster title, mortgage, attachment and limited-rights
   information. Record erfpacht, opstal and servitudes rather than
   treating silence as ownership free of restrictions.
3. Classify the property: residential/commercial, owner-occupied/rented,
   apartment/VvE, private/corporate owner, and existing mortgage. For
   every conditional branch attach its evidence or a human-verified
   not-applicable declaration.
4. Assemble known-defect, municipal permit/environment-plan, energy-label,
   VvE, erfpacht and tenancy evidence. A valid EP-online label or a
   documented statutory exemption is required.
5. Draft transaction terms and record whether BW Book 7 article 2 applies.
   If it does, preserve delivery of the signed written agreement and the
   three-day cooling-off timeline as evidence.
6. Screen all natural-person and corporate parties. Give the notary the
   identity, authority, UBO and source-of-funds material requested for the
   notary's independent Wwft review. An actor pre-screen is not a substitute.
7. Select the notary and send the complete closing package. Obtain the
   concept `akte van levering`, mortgage redemption/discharge statement,
   closing statement and funds-flow instructions.
8. Run `:jurisdiction/assess`; a human reviews and approves the committed
   checklist. Run `:closing/submit` only after every checklist item is
   evidenced and all party KYC results are clean.
9. `:closing/submit` always escalates. The notary performs final registry
   checks, executes the deed, submits it to Kadaster, verifies registration
   and alone releases the proceeds. Store the resulting references as
   external evidence; never claim the actor issued registered title.

## Mandatory holds

- unknown or mismatched owner/parcel;
- unresolved mortgage, attachment or limited right;
- missing co-owner/corporate authority;
- missing applicable energy-label, VvE, erfpacht or tenancy evidence;
- sanctions/PEP hit or incomplete notary Wwft review;
- no selected notary or no notary-approved deed draft;
- any request for autonomous deed execution, registration or funds release.

## Official source set

- Kadaster transfer flow: <https://www.kadaster.nl/situaties/regelen-via-de-notaris/akte-inschrijven-bij-koop-van-een-huis>
- Dutch Civil Code Book 3: <https://wetten.overheid.nl/BWBR0005291/>
- Dutch Civil Code Book 7: <https://wetten.overheid.nl/BWBR0005290/>
- RVO energy labels: <https://www.rvo.nl/onderwerpen/wetten-en-regels-gebouwen/energielabel-woningen>
- KNB/Wwft: <https://www.knb.nl/ons-beroep/toezicht-tuchtrecht/wet-en-regelgeving/wwft>

Re-verify these sources and municipality-specific rules at intake and
again before closing; the catalog is not a frozen statement of future law.
