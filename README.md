# ADG
# Railway Ticket Booking System

A command-line ticket booking system built in Python. You pick a route, a train, a class, enter your passengers, and it gives a full fare breakdown with baggage charges and promo code support.

## Project Structure

railway:-
 >main.py            # Entry point, ties everything together
 >routes.py          # Route distances, train types, class info, promo codes
 >fare.py            # All the math
 >display.py         # Terminal output and formatting
 >input_helpers.py   # Input collection with validation
 >README.md

## What to Expect

The program walks you through everything step by step:

1. Pick your origin and destination (5 cities, 10 routes)
2. Choose a train type — Superfast, Express, or Fast Passenger
3. Choose a travel class — Sleeper, AC 3-Tier, or AC 2-Tier
4. Enter details for each passenger (name, age) — up to 6
5. Declare baggage weight per passenger
6. Optionally apply a promo code at the end

It'll handle bad inputs without crashing — wrong types, out-of-range numbers, empty names, negative weights, all covered.

## Promo Codes
ADG20      - 20% off the subtotal       
WINTER500  - Flat INR 500 off the total 

Only one code per booking. Invalid codes are flagged and ignored.

## How Fares Are Calculated

Each passenger is calculated individually, in this order:

1. Slab-based distance fare (INR 100 base + per-km rates by distance band)
2. 40% discount if the passenger is over 60
3. Train type premium multiplied on
4. Travel class multiplier applied
5. Excess baggage charged at INR 15/kg over the free allowance
6. Flat surcharge added based on train type
INR 15/kg over the free allowance
