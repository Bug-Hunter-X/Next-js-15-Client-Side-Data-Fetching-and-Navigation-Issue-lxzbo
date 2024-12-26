# Next.js 15 Client-Side Data Fetching and Navigation Issue

This repository demonstrates a bug in Next.js 15 related to client-side data fetching and unexpected behavior when navigating between pages.

## Bug Description

A counter on the `/about` page continues to increment even after navigating away from the page and returning. This is due to the `useEffect` hook and `setInterval` not properly cleaning up when the component unmounts.

## Reproduction Steps

1. Clone this repository.
2. Run `npm install`.
3. Run `npm run dev`.
4. Navigate to `/about`.
5. Observe the counter incrementing.
6. Navigate to `/`.
7. Navigate back to `/about`.
8. Observe that the counter continues to increment from where it left off.

## Solution

The solution involves ensuring that the `setInterval` is properly cleared when the component unmounts to prevent the counter from continuing to increment unexpectedly. See the solution file for the corrected code.