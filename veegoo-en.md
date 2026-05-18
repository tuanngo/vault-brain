---
type: Project
status: Active
relationships:
  Type:
    - "[[project]]"
  related_to:
    - "[[Veegoo]]"
_organized: true
---
# Veegoo (English)

**Veegoo** is a SaaS Transport Management System (TMS) built for independent transport operators, business fleets, and employee shuttle services. Veegoo simplifies route, vehicle, customer, and driver management — all in one place.

## Overview

Veegoo solves the daily operational challenges faced by small and mid-sized transport operators: real-time vehicle tracking, schedule and route management, customer bookings, and coordination with partner operators when vehicles have empty seats. The platform supports both a **solo model** (one person managing their own vehicle) and a **collaborative model** (multiple operators sharing routes and revenue).

At the **MVP stage**, the focus is on individuals or small teams: a single owner-operator can run their own vehicles, register routes, accept bookings, and expand into partner sharing as needed.

## Goals

- **Simplify operations** — enable one person to manage all their transport activity without an administrative team.
- **Reduce empty runs** — connect independent operators to share routes and fill seats, cutting dead-mileage trips.
- **Transparent revenue sharing** — automatically calculate and distribute earnings when operators collaborate.
- **Scale gradually** — from solo MVP operators to enterprise fleet management and industrial-zone employee shuttles.

## Target Users

| User | Role |
|---|---|
| **Owner / Business Operator** | Manages all activity: vehicles, routes, revenue, and partner relationships |
| **Dispatcher** | Assigns drivers, monitors schedules, and handles day-to-day operational issues |
| **Driver** | Receives schedules, views routes, and updates trip status |
| **Passenger / Employee** | Books seats, views trip details, and tracks the arriving vehicle |

> **MVP focus:** The solo owner-operator — someone who is both owner and dispatcher, possibly running just 1–2 vehicles.

## Key Concepts

### Route
A fixed or flexible journey between a pickup point and a drop-off point. A route may be operated by a single operator or shared with a partner operator.

### Trip
A specific run on a route, linked to a driver, vehicle, departure time, and passenger manifest.

### Booking
A customer request to join a specific trip. The system confirms, allocates seats, and sends notifications automatically.

### Partner Sharing
When an operator's vehicle has spare capacity, they can invite a partner operator to fill seats or hand off the route. Revenue splits are calculated and distributed automatically based on the agreed ratio.

### Operator
The operating entity — can be an individual owning a single vehicle or a company running a large fleet. Each Operator has an isolated workspace (multi-tenant).

## Key Features

- **Route & trip management** — create and edit schedules and routes flexibly
- **Customer bookings** — booking form, automatic confirmation, passenger manifest
- **Partner sharing** — route sharing and revenue splitting between partner operators
- **Real-time vehicle tracking** — GPS tracking, live trip status
- **Operations dashboard** — overview of revenue, active trips, vehicles, and drivers
- **Driver app** *(Next phase)* — receive schedules and update status from mobile
- **Multi-tenant** — each operator has isolated data and access controls
