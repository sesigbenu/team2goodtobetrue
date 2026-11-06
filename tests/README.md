# Testing

## What We Plan to Test
We plan to test the system in three layers. The first focuses on individual
pieces of the backend, such as the logic that checks room availability and
the 2 minute blackout window. The second focuses on how the backend works
with our Azure SQL Database, especially to confirm that two users cannot
book the same room at the same time. The third focuses on the full booking
experience from the user's point of view, including searching, selecting,
completing the blackout window, and confirming a reservation.

## Situations We Want to Catch Early
A room should be released back into the system if the user does not confirm
within the 2 minute window. When two users try to book the same room at the
same time, only one booking should be confirmed. Any failure from an
external UMD reservation site should be reported back to the user clearly
rather than silently failing.

## Next Steps
Once the first reservation endpoint is ready, we will begin writing tests
against it.