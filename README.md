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
//2024-05-27 13:09:59
```
Or
```bash
const datetime = new DateTime();
datetime.now().format().value;
//2024-05-27 13:09:59
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