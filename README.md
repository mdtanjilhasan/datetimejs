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