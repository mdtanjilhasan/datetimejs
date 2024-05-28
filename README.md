# datetimejs
A simple DateTime Package based on dayjs

# Installation
```bash
npm i tanjil-datetime
```

# Uses
import this in your project
```bash
import DateTime from "tanjil-datetime";
```
#### Initialization
```bash
DateTime.init().now().format().value;
// 2024-05-27 13:09:59
```
Or
```bash
const datetime = new DateTime();
datetime.now().format().value;
// 2024-05-27 13:09:59
```
#### List of all available formats

```bash
DateTime.init().now().format('YYYY-MM-DD hh:mm:ss A').value
// 2024-05-27 02:06:21 PM
```

<table>
    <thead>
        <tr>
            <th>Format</th>
            <th>Output</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><code>YY</code></td>
            <td>18</td>
            <td>Two-digit year</td>
        </tr>
        <tr>
            <td><code>YYYY</code></td>
            <td>2018</td>
            <td>Four-digit year</td>
        </tr>
        <tr>
            <td><code>M</code></td>
            <td>1-12</td>
            <td>The month, beginning at 1</td>
        </tr>
        <tr>
            <td><code>MM</code></td>
            <td>01-12</td>
            <td>The month, 2-digits</td>
        </tr>
        <tr>
            <td><code>MMM</code></td>
            <td>Jan-Dec</td>
            <td>The abbreviated month name</td>
        </tr>
        <tr>
            <td><code>MMMM</code></td>
            <td>January-December</td>
            <td>The full month name</td>
        </tr>
        <tr>
            <td><code>D</code></td>
            <td>1-31</td>
            <td>The day of the month</td>
        </tr>
        <tr>
            <td><code>DD</code></td>
            <td>01-31</td>
            <td>The day of the month, 2-digits</td>
        </tr>
        <tr>
            <td><code>d</code></td>
            <td>0-6</td>
            <td>The day of the week, with Sunday as 0</td>
        </tr>
        <tr>
            <td><code>dd</code></td>
            <td>Su-Sa</td>
            <td>The min name of the day of the week</td>
        </tr>
        <tr>
            <td><code>ddd</code></td>
            <td>Sun-Sat</td>
            <td>The short name of the day of the week</td>
        </tr>
        <tr>
            <td><code>dddd</code></td>
            <td>Sunday-Saturday</td>
            <td>The name of the day of the week</td>
        </tr>
        <tr>
            <td><code>H</code></td>
            <td>0-23</td>
            <td>The hour</td>
        </tr>
        <tr>
            <td><code>HH</code></td>
            <td>00-23</td>
            <td>The hour, 2-digits</td>
        </tr>
        <tr>
            <td><code>h</code></td>
            <td>1-12</td>
            <td>The hour, 12-hour clock</td>
        </tr>
        <tr>
            <td><code>hh</code></td>
            <td>01-12</td>
            <td>The hour, 12-hour clock, 2-digits</td>
        </tr>
        <tr>
            <td><code>m</code></td>
            <td>0-59</td>
            <td>The minute</td>
        </tr>
        <tr>
            <td><code>mm</code></td>
            <td>00-59</td>
            <td>The minute, 2-digits</td>
        </tr>
        <tr>
            <td><code>s</code></td>
            <td>0-59</td>
            <td>The second</td>
        </tr>
        <tr>
            <td><code>ss</code></td>
            <td>00-59</td>
            <td>The second, 2-digits</td>
        </tr>
        <tr>
            <td><code>SSS</code></td>
            <td>000-999</td>
            <td>The millisecond, 3-digits</td>
        </tr>
        <tr>
            <td><code>Z</code></td>
            <td>+05:00</td>
            <td>The offset from UTC, ±HH:mm</td>
        </tr>
        <tr>
            <td><code>ZZ</code></td>
            <td>+0500</td>
            <td>The offset from UTC, ±HHmm</td>
        </tr>
        <tr>
            <td><code>A</code></td>
            <td>AM PM</td>
            <td></td>
        </tr>
        <tr>
            <td><code>a</code></td>
            <td>am pm</td>
            <td></td>
        </tr>
    </tbody>
</table>

# Parsing

```bash
DateTime.init().parse(new Date()).format().value
// 2024-05-27 13:10:11
```
Or
```bash
DateTime.init().parse(DateTime.init().now().value).format().value
// 2024-05-27 13:10:20
```
Or
```bash
DateTime.init().parse('2022').format().value
// 2022-01-01 00:00:00
```
Or
```bash
DateTime.init().parse('2022-05').format().value
// 2022-05-01 00:00:00
```
Or
```bash
DateTime.init().parse('2022-05-08').format().value
// 2022-05-08 00:00:00
```
Or
```bash
DateTime.init().parse('10:55:10').format().value
// 2024-05-27 10:55:10
```
Or
```bash
DateTime.init().parse('20:55:10').format('YYYY-MM-DD hh:mm:ss A').value
// 2024-05-27 08:55:10 PM
```
Or
```bash
DateTime.init().parse('2023-05-04 20:55:10').format('YYYY-MM-DD hh:mm:ss A').value
// 2023-05-04 08:55:10 PM
```

# Addition

Add One Day
```bash
DateTime.init().now().addDay().format().value
// 2024-05-28 13:19:59
```
Add More than one Day
```bash
DateTime.init().now().addDays(2).format().value
// 2024-05-29 13:20:50
```
#### List of all methods

<table>
    <thead>
        <tr>
            <th>Method</th>
            <th>Params</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><code>addDay</code></td>
            <td>--</td>
            <td>Add One Day to a date</td>
        </tr>
        <tr>
            <td><code>addDays</code></td>
            <td>count as integer: example <code>addDays(5)</code></td>
            <td>Add custom day count to a date</td>
        </tr>
        <tr>
            <td><code>addWeek</code></td>
            <td>--</td>
            <td>Add One Week to a date</td>
        </tr>
        <tr>
            <td><code>addWeeks</code></td>
            <td>count as integer: example <code>addWeeks(5)</code></td>
            <td>Add custom week count to a date</td>
        </tr>
        <tr>
            <td><code>addMonth</code></td>
            <td>--</td>
            <td>Add One month to a date</td>
        </tr>
        <tr>
            <td><code>addMonths</code></td>
            <td>count as integer: example <code>addMonths(5)</code></td>
            <td>Add custom month count to a date</td>
        </tr>
        <tr>
            <td><code>addYear</code></td>
            <td>--</td>
            <td>Add One year to a date</td>
        </tr>
        <tr>
            <td><code>addYears</code></td>
            <td>count as integer: example <code>addYears(5)</code></td>
            <td>Add custom year count to a date</td>
        </tr>
        <tr>
            <td><code>addHour</code></td>
            <td>--</td>
            <td>Add One hour to a time</td>
        </tr>
        <tr>
            <td><code>addHours</code></td>
            <td>count as integer: example <code>addHours(5)</code></td>
            <td>Add custom hour count to a time</td>
        </tr>
        <tr>
            <td><code>addMinute</code></td>
            <td>--</td>
            <td>Add One minute to a time</td>
        </tr>
        <tr>
            <td><code>addMinutes</code></td>
            <td>count as integer: example <code>addMinutes(5)</code></td>
            <td>Add custom minute count to a time</td>
        </tr>
        <tr>
            <td><code>addSecond</code></td>
            <td>--</td>
            <td>Add One second to a time</td>
        </tr>
        <tr>
            <td><code>addSeconds</code></td>
            <td>count as integer: example <code>addSeconds(5)</code></td>
            <td>Add custom second count to a time</td>
        </tr>
    </tbody>
</table>