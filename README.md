# Tara Hotel OS

An applied-AI portfolio exploring how independent hotels can use agents across guest service, operations, and revenue—without removing human control.

This work is led by Rupesh Zavar, an independent hotel owner/operator with roughly 15 years of operating experience. The projects are grounded in two active hotels that provide real environments for testing workflows, staff handoffs, operational exceptions, and measurable outcomes.

## The operating thesis

Independent hotels rarely lack software. They lack a shared operating layer that can understand context across disconnected systems, surface the next useful action, route exceptions, and preserve accountability.

Tara OS is an exploration of that layer: agents assist the people running the hotel, while staff retain approval and escalation control.

## Active projects

### Tara OS

The coordinating operating layer. It connects signals from guest interactions, reservations, room readiness, hotel operations, and revenue workflows so each specialist system can act with the right context.

**Current experiment:** define safe, property-specific workflows and a common pattern for evidence, recommendations, approval, action, and read-back.

### Symphia

An AI voice agent for guest calls and hotel-specific questions. It identifies intent, retrieves relevant property information, routes requests, and escalates to a person when confidence or authority is insufficient.

**Current experiment:** improve intent detection, answer quality, routing, and handoff summaries while making uncertainty explicit.

### Revenue MVP

AI-assisted revenue and pricing intelligence. It monitors occupancy, pickup, cancellations, inventory and rate gaps, and market conditions to surface pricing actions for review.

**Current experiment:** turn fragmented signals into an evidence-backed daily decision queue, with recommendations separated clearly from approved changes.

### Digital Guest Journey

Connected workflows spanning pre-arrival, self-check-in, room readiness, in-stay requests, stay extensions and late checkout, folio review, and checkout.

**Current experiment:** reduce friction and missed handoffs while preserving a clear path to hotel staff.

### Operations Engine

A system for capturing real hotel problems, identifying repeatable patterns, turning those patterns into workflows and rules, measuring exceptions, and progressively automating what proves reliable.

**Current experiment:** build a disciplined feedback loop from frontline issue to observable workflow improvement.

## Conceptual architecture

~~~mermaid
flowchart LR
    A[Hotel signals] --> B[Property context and evidence]
    B --> C[Specialist agents]
    C --> D[Recommendation or routed request]
    D --> E{Human review needed?}
    E -->|Yes| F[Approve, edit, or escalate]
    E -->|No, within policy| G[Execute bounded workflow]
    F --> G
    G --> H[Verify outcome and record exception]
    H --> B
~~~

The design keeps four boundaries explicit:

1. **Evidence:** what the system actually knows, including missing or stale inputs.
2. **Authority:** what an agent may recommend, what requires approval, and what it may execute.
3. **Property isolation:** hotel-specific context, rules, and integrations remain separated.
4. **Verification:** actions are checked after execution, and exceptions feed the next iteration.

## Development approach

The portfolio follows a staged path:

**Observe → Recommend → Approve → Act → Verify → Learn**

Early experiments emphasize usefulness and safety over broad autonomy. Success means fewer missed handoffs, faster response, clearer decisions, and better outcomes—not simply more automation.

## What is intentionally not public

This repository is a high-level portfolio, not a production deployment. It does not contain credentials, guest information, private hotel data, proprietary integrations, internal operating rules, or sensitive infrastructure details.
