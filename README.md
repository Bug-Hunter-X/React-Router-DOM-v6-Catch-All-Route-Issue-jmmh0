# React Router DOM v6 Catch-All Route Issue

This repository demonstrates an unexpected behavior with the catch-all route (`/*`) in React Router DOM v6. The issue occurs when combining a catch-all route with other specific routes.  The catch-all route seems to override other routes, even though it should only match when no other route matches.

## Steps to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Navigate to `/` - it will correctly show the Home component
5. Navigate to `/about` - it will correctly show the About component
6. Navigate to any other route, such as `/contact` - it should display the Not Found component but it doesn't work as expected.

## Solution

The solution involves the order of the routes. The catch-all route must be placed at the end of the route definitions so that the other routes are matched first and the catch all route will match if no specific routes are matched. Refer to `AppSolution.js` for the solution.
