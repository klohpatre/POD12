# PITCH.md

Six lines and a lever. Your words. The last two are scored.

Built: A disruption-care agent for Larkspur that reads a booking, checks the live
flight, and answers from the policy row instead of from memory.

Does: Tells a stranded customer what they are actually owed, holds a seat without
booking it, and hands the file to a named human when the conversation stops being
about the flight.

Number: 1,549 tokens of tool schema on every turn, 10 tools, n=5 cases averaging
3.6 turns and 12.0s each, counted on the wire.

Guardrail: It will not confirm a rebooking on a chat message. A held seat needs
the customer's own Confirm-click, and "I authorise it" does not mint that token.

Next: Trim the schema tax. Ten tools ride on every turn whether the case needs
them or not, and we have never measured what fewer would cost us.

Still broken: The tone rule was written from the outside, not from Larkspur's own
words, so it fires on two conditions we guessed at rather than ones the contact
centre gave us.

Lever: intelligence

## Priya asked

Costs: 1,549 schema tokens per turn is the floor before anyone says anything, and
it scales with turns, not with customers helped.

Wrong: It escalated an ordinary angry customer once, because our first tone rule
read "hostility" too broadly. The eval caught it; nobody in the room did.

Runs it: Whoever owns the policy rows, because every refusal this agent makes
cites one and goes stale when the row changes.

Left out: We never measured cost or latency against a baseline, so the schema
number is a fact about our build, not a saving we can claim.
