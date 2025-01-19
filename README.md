# React Router v6 Route Path Substring Issue

This repository demonstrates a subtle bug in React Router v6 related to route path conflicts when one path is a substring of another.

## Problem

The `App.js` file contains a simple React Router setup. Notice that the path `/contact` is a substring of `/contact-us`.  When navigating to `/contact`, only the Home component renders instead of the Contact component.  This is because the routing logic matches `/contact` before proceeding to `/contact-us`.

## Solution

The `AppSolution.js` file demonstrates how to solve this issue by using more specific and less ambiguous route paths. The solution adds more detail to the path specification.  This ensures that the routes don't conflict and each will render appropriately.