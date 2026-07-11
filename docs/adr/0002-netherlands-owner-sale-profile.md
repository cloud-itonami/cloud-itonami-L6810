# ADR-0002: Netherlands owner-sale closing profile

- Status: accepted
- Date: 2026-07-11

## Context

The 6810 actor already governed listing intake, jurisdiction assessment,
party screening and human-approved closing drafts, but NLD had no official
spec-basis. The separate `cloud-itonami-iso3166-nld` actor covers market
entry/procurement and cannot by itself establish Dutch real-property title.

## Decision

Add NLD to `realty.facts` as the transaction-law profile and keep the
country actor as an optional source for operator/business identity. The
NLD checklist cites Dutch legislation, Kadaster, RVO and the notarial AML
framework. Conditional VvE, erfpacht, mortgage and tenancy branches require
evidence or an explicit human-verified not-applicable declaration.

Model the Dutch notary and Kadaster boundary as data (`:actuation-authority`
and `:human-gates`) in addition to the existing structural invariant that
`:closing/submit` never auto-commits. The actor prepares a draft package;
it never executes the deed, registers title or releases funds.

## Consequences

- NLD assessment and closing drafts can use a sourced checklist rather
  than being held as an unknown jurisdiction.
- A broker remains optional; a Netherlands civil-law notary does not.
- Municipality-, property- and tax-specific decisions remain outside this
  generic profile and require current human professional review.
- Future connectors return evidence only; they must not weaken the governor
  or translate an external API success into autonomous actuation.
