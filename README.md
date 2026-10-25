# Kurty

Kurty is a mobile app concept for Morocco's grand taxi ecosystem, connecting kourtis, drivers, and passengers.

**Status:** Brainstorming and product definition. No application code or technology stack has been chosen yet. This README records the discussion so far; proposed details below are not final decisions.

## Core idea

The **kourti is the main operator**. They manage taxis, drivers, destinations, and the departure order, then create trips that passengers can join. Drivers have their own accounts and profiles, and the kourti can see taxi locations.

## Vocabulary

- **Kourti:** The person who manages grand taxis and coordinates their operation, as described for this project.
- **Nouba:** The order of turns — “who comes after whom.” The kourti sets this order for the taxis.
- **Fayaje:** The working name for a trip or departure event created by the kourti. Passengers fill its available seats before the taxi leaves. The name is provisional.

## Requirements discussed

### Kourti

- Maintain the taxi and driver roster, including taxi matricule (registration number), driver ID, and phone number.
- Add or delete drivers as needed.
- Set the nouba and taxi destinations.
- Create and manage Fayajes.
- Publish taxi and trip availability for passengers.
- See taxi locations.

### Driver

- Have an account and driver profile linked to their taxi information.
- Participate in the nouba and operate assigned Fayajes.
- Provide location information for the kourti; the sharing mechanism and permissions remain to be designed.

### Passenger

- View available taxis and destination information maintained by the kourti.
- Join a Fayaje and fill its available seats.
- Use that information to plan travel to the departure station.

The exact meaning of joining a Fayaje — reservation, request, or confirmed seat — is still open.

## Proposed workflow — pending validation

1. The kourti maintains the driver/taxi roster and sets the nouba and destinations.
2. The next eligible driver confirms availability for a destination.
3. The kourti opens a Fayaje with an assigned taxi, departure station, destination, and available seats.
4. Passengers join through the app. The kourti can also record passengers who arrive in person.
5. Once all seats are allocated, the Fayaje is marked fully reserved.
6. The kourti checks that passengers are present. The driver then marks departure.
7. The trip is eventually marked completed, and the taxi's availability is updated.

### When should the driver accept the destination?

**Current recommendation, not yet confirmed:** Obtain the driver's commitment before opening the Fayaje to passengers. Confirm departure separately once passengers are present.

A driver could confirm their destination and availability at the start of a shift, avoiding repeated acceptance for every trip. Waiting until a Fayaje fills up to seek driver acceptance risks leaving passengers without a willing driver and disrupting the nouba.

If passengers express interest before a driver is assigned, that could be represented as a waiting list rather than a confirmed Fayaje.

### Proposed trip states

`Draft → Open for passengers → Fully reserved → Ready to depart → Departed → Completed`

These states are a starting point. Cancellation, driver replacement, and reopening seats need explicit rules. Fully reserved does not automatically mean passengers have arrived.

## Suggested first pilot — not yet agreed

Start with one station and a few routes, covering the three roles:

- Kourti roster, nouba, and Fayaje management.
- Driver accounts, profiles, and availability confirmation.
- Passenger destination search, availability, and joining a Fayaje.
- Simple seat updates that include passengers arriving in person.
- Taxi location sharing with the kourti, with driver control over when sharing is active.

Suggested usability details include one-tap seat updates, a visible last-updated time, and marking stale availability as unconfirmed. Removing a driver from today's nouba should be separate from deleting their profile. These are proposals to validate with actual station operations.

## Open questions

1. Is there a separate nouba for each destination, or one shared queue?
2. Who chooses a driver's destination, and when is that commitment confirmed?
3. Does joining a Fayaje reserve a seat immediately, or require kourti approval?
4. How are online passengers and passengers arriving in person counted without overbooking?
5. How long is a seat held, and what happens if a passenger cancels or does not arrive?
6. What happens if a driver declines, becomes unavailable, or needs replacement? How does that affect their place in the nouba?
7. Who can edit the nouba, and how are changes communicated to drivers?
8. When is location shared, and who can see it? Passenger access to live taxi locations has not been agreed.
9. What does “driver ID” mean for this product, and which profile fields are visible to each role?
10. What are the fare, payment, and revenue models? None has been selected.
11. Which languages and mobile platforms should the first version support?
12. Which station and routes would be suitable for a first pilot?

## Next step

Walk through a real station's day with a kourti and a driver. Resolve the nouba structure and seat-confirmation rules, then sketch the main screens and choose the first implementation scope.
