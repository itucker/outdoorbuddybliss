# Product Requirements Document (PRD) — OutdoorBuddyBliss (Draft)

## 1. Overview
Purpose: Define MVP features, acceptance criteria, and milestones to deliver the initial product for planning and booking local outdoor experiences.

## 2. Goals & success criteria
- Launch an MVP that enables users to discover listings, create trip plans, invite friends, and book or contact a local operator.
- Baseline KPIs: onboarding conversion, trip plan creation, bookings through platform.

## 3. Scope (MVP)
Included:
- Listings: curated trails/experiences with photos, difficulty, distance, and partner contact
- Trip planner: create a trip, date, time, invite friends (email/username), packing checklist
- Social invites & RSVPs: simple invite flow and RSVP state
- Partner profiles: small operator profiles, contact or booking request
- Basic search & filters (distance, difficulty, tags)
- Admin dashboard: add/edit listings and view bookings (basic)

Out of scope (MVP):
- Payments processing (use contact/booking request workflow first)
- Advanced routing/GPS turn-by-turn navigation
- Full marketplace with dynamic pricing

## 4. User personas & user stories
Persona A — Weekend Planner:
- As a planner, I want to find a nearby easy hike and invite 3 friends so we can go this Saturday.
Acceptance: Search within 30 miles, filter by difficulty = easy, create trip, invite 3 emails, RSVPs tracked.

Persona B — Local Guide:
- As a guide, I want to list a guided tour and receive booking requests.
Acceptance: Guide profile created, receives booking requests by email/dashboard.

## 5. Functional requirements (high-level)
- Listings API: create/read/listing with metadata (title, description, difficulty, coords, tags)
- Planner UI: create trip object with participants, date, checklist
- Notifications: email/in-app invitations and reminders (day-before)
- Admin UI: CRUD for listings + view requests

## 6. Non-functional requirements
- Auth: OAuth + email sign-up
- Performance: search results < 1s average
- Privacy & Security: store minimal PII, GDPR-conscious defaults

## 7. Acceptance criteria & test cases
- Create trip: trip saved, invites sent, invitee can RSVP and see trip details
- Listing search: filters return expected subset in < 1s
- Partner request flow: submitting a booking request triggers email notification to partner address

## 8. Data definitions
- Listing: id, title, slug, description, difficulty, coordinates, images[], partner_id
- Trip: id, owner_id, date, participants[], checklist[], status

## 9. Milestones & roadmap
- Week 0–2: Discovery, wireframes, schema design
- Week 3–8: Implement core APIs and planner UI
- Week 9–12: Partner onboarding + pilot testing

## 10. Open questions
- Payment timeline: when to integrate payments?
- Pilot city and partner recruitment resources

## 11. Appendix
- Links to wireframes, research notes (to be added)