# Rapido Clone — Customer & Captain Frontends

Responsive React + TypeScript + Vite starter for a ride-hailing portfolio project. These screens currently use local mock data; authentication, maps, booking, location updates, and payments are not connected to a backend yet.

## Requirements
- Node.js 20+ (Node 22 LTS recommended)
- npm 10+

## Run locally
From the repository root:

```bash
npm install
npm run dev:customer
```

Open the URL printed by Vite (normally http://localhost:5173). In another terminal:

```bash
npm run dev:captain
```

Vite selects another port if 5173 is already occupied (often 5174).

## Build both apps

```bash
npm run build
```

Build outputs are created under each app's `dist/` directory.

## Frontend routes / demo interactions
- Customer: choose pickup and destination, select Bike/Auto, see a mock fare, request a ride, and cancel the local demo ride.
- Captain: switch online/offline, accept/reject a mock request, progress a trip, and view demo earnings.

## Next integration steps
1. Add Spring Boot API endpoints and configure `VITE_API_BASE_URL` per environment.
2. Replace demo actions with API calls and handle loading/error states.
3. Add Cognito/OIDC or a secure backend auth flow; don't store sensitive tokens in local storage for a production application.
4. Add Google Maps/Mapbox using environment-injected keys and domain restrictions.
5. Add unit tests, accessibility checks, and Playwright end-to-end tests.
6. Build separate Docker images and publish them to Amazon ECR; deploy behind an AWS Load Balancer Controller/Ingress on EKS.

## Security note
Never commit real API keys, credentials, payment secrets, or AWS access keys. The UI is a portfolio starter, not a production-ready transport/payment service.
