# React Router Dom v6 Catch-All Route (*) Issue

This repository demonstrates a common issue encountered when using catch-all routes ("/*") in React Router Dom v6.  The catch-all route unexpectedly intercepts requests, even when a more specific route should handle them. 

The problem arises from the order of routes defined within the `<Routes>` component.  The catch-all route should always be placed last to ensure it functions as intended.  This example shows both the erroneous and the correct implementation.

## How to reproduce
1. Clone the repository.
2. Run `npm install` to install the dependencies.
3. Run `npm start` to start the development server. 
4. Navigate to `/about` - you should see the 'About' page, as expected. 
5. Now try navigating to `/` - this also matches the catch all route, showing the bug.  This should show the 'Home' page. 
6. Review the 'AppSolution.js' file for the solution. 