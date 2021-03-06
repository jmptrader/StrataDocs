---
title: Standard Reference Data
permalink: /standard_ref_data/
---

Strata provides a set of standard reference data, including holidays, indices and conventions.

## Holiday calendars

Each holiday calendar represents a consistent set of weekends and holidays.
In most cases they refer to a specific location, however some calendars are location independent.

The intention of providing these calendars is to allow the system to be easily evaluated.
When using this library in production, OpenGamma strongly recommends replacing the data provided
with data from an external vendor of holiday information.

The holiday dates are based on original research and typically cover 1950 to 2099.
Future and past dates are an extrapolations of the known holiday dates.

| Name | Holidays                                         | Weekends          | ISDA reference      |
|------|--------------------------------------------------|-------------------|---------------------|
| AUSY | Sydney (Australia) holidays                      | Saturday/Sunday   |                     |
| CATO | Toronto (Canada) holidays                        | Saturday/Sunday   |                     |
| CHZU | Zurich (Switzerland) holidays                    | Saturday/Sunday   |                     |
| EUTA | TARGET interbank payment (Europe) holidays       | Saturday/Sunday   | section 1.8 (2006)  |
| FRPA | Paris (France) holidays                          | Saturday/Sunday   |                     |
| GBLO | London (UK) holidays                             | Saturday/Sunday   |                     |
| JPTO | Tokyo (Japan) holidays                           | Saturday/Sunday   |                     |
| NOOS | Oslo (Norway) holidays                           | Saturday/Sunday   |                     |
| NYFD | Federal Reserve Bank of New York holidays        | Saturday/Sunday   | section 1.9 (2006)  |
| NYSE | New York Stock Exchange holidays                 | Saturday/Sunday   | section 1.10 (2006) |
| USGS | United States Government Securities              | Saturday/Sunday   | section 1.11 (2006) |
| USNY | New York (USA) holidays                          | Saturday/Sunday   |                     |
|------------|----------------------|-------------------|----|
| NoHolidays | No holiday dates     | No weekends       |    |
| Sat/Sun    | No holiday dates     | Saturday/Sunday   |    |
| Fri/Sat    | No holiday dates     | Friday/Saturday   |    |
| Thu/Fri    | No holiday dates     | Thursday/Friday   |    |

Holiday calendars have a constant in `HolidayCalendarIds`.
The identifier can also be created dynamically using `HolidayCalendarId.of(name)`.


## Indices

Strata includes constants and definitions for many common indices.
These represent the correct convention to our best knowledge at the time of coding.

Overnight Indices:

| Name           | Description              | Day Count    |
|----------------|--------------------------|--------------|
| AUD-AONIA      | AONIA index for AUD      | Act/365F     |
| CAD-CORRA      | CORRA index for CAD      | Act/365F     |
| CHF-TOIS       | TOIS index for CHF       | Act/360      |
| EUR-EONIA      | EONIA index for EUR      | Act/360      |
| GBP-SONIA      | SONIA index for GBP      | Act/365F     |
| NOK-NOWA       | NOWA index for NOK       | Act/Act Year |
| JPY-TONAR      | TONAR index for JPY      | Act/365F     |
| USD-FED-FUND   | Fed-Fund index for USD   | Act/360      |

Ibor Indices:

| Name                 | Tenors                   | Description               | Day Count    |
|----------------------|--------------------------|---------------------------|--------------|
| AUD-BBSW-XX          | 1M,2M,3M,4M,5M,6M        | BBSW index for AUD        | Act/365F     |
| CAD-CDOR-XX          | 1M,2M,3M,6M,12M          | CDOR index for CAD        | Act/365F     |
| CHF-LIBOR-XX         | 1W,1M,2M,3M,6M,12M       | LIBOR index for CHF       | Act/360      |
| EUR-LIBOR-XX         | 1W,1M,2M,3M,6M,12M       | LIBOR index for EUR       | Act/360      |
| EUR-EURIBOR-XX       | 1W,2W,1M,2M,3M,6M,9M,12M | EURIBOR index for EUR     | Act/360      |
| GBP-LIBOR-XX         | 1W,1M,2M,3M,6M,12M       | LIBOR index for GBP       | Act/365F     |
| JPY-LIBOR-XX         | 1W,1M,2M,3M,6M,12M       | LIBOR index for JPY       | Act/360      |
| JPY-TIBOR-JAPAN-XX   | 1W,1M,2M,3M,6M,12M       | TIBOR index for JPY       | Act/365F     |
| JPY-TIBOR-EUROYEN-XX | 1W,1M,2M,3M,6M,12M       | TIBOR index for JPY       | Act/360      |
| NOK-NIBOR-XX         | 1W,1M,2M,3M,6M           | NIBOR index for NOK       | Act/360      |
| USD-LIBOR-XX         | 1W,1M,2M,3M,6M,12M       | LIBOR index for USD       | Act/360      |

To get the name of the index, replace "XX" with one of the tenors.
For example, "GBP-LIBOR-3M" is a valid index name.

