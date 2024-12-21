# React Router v6 Catch-all Route Issue

This repository demonstrates a common issue encountered when using catch-all routes (`/*`) in React Router v6. The catch-all route, intended to handle unmatched routes, is incorrectly intercepting other defined routes.  The problem is that the catch-all route is too broad, matching everything before the more specific routes are even considered.

## Problem

The provided `App.js` shows the standard setup where a catch-all route `/` is used to show 404 error page.  However this conflicts with other routes causing the 404 to always be displayed.

## Solution

The solution in `AppSolution.js` demonstrates how to correct this by rearranging the order of the routes.  Specific routes should always be defined *before* the catch-all route in React Router v6. This ensures that more specific paths are checked first.