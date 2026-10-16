# Operational interface recipes

## Sign-in form

Show a heading that explains the next step and use a label in addition to the placeholder. Separate external providers from the email path when both exist. A disabled button must have an understandable reason; after submitting, show the real state and the next action. Preserve inputs on error and do not clear the screen before the result is confirmed.

## Calculator

Input and result stay close in reading order. Define unit, currency, limits and rounding rule. Changing the mode must update the explanation and result coherently. Unknown data is not zero. Estimated results must be labeled; do not announce updates on every keystroke if that makes a screen reader unusable.

## Proposed operational listing

The pattern below is an original proposal, not an observation of the AbacatePay dashboard.

Filters affect the listing and expose the current state. The initial empty state guides creation/import; zero results guides clearing filters. A query error must not look like an empty list. A row shows identifier, main information, status and a contextual action; status includes text.

Multiple selection requires an understandable selected count, scope and action. Formatting tabular values and aligning decimal places makes comparison easier. On mobile, do not drop decisive data just to make everything fit.

## Confirmation and updates

A pending response must stay pending until the backend confirms it. Animating a checkmark does not change the state. Provide enough detail to check the operation and recovery when it fails. Disabling the action while submitting can reduce repeated clicks, but real duplicate prevention also depends on product logic.

## Brazilian Portuguese copy

Prefer specific verbs: criar, copiar, filtrar, salvar, tentar novamente (create, copy, filter, save, try again). Avoid labels like “Continuar” (Continue) when “Revisar cobrança” (Review charge) makes the next step clearer. Do not sacrifice currency/date precision for overly casual copy.
