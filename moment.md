## To Find different between two timestamps
```js
const timestamp = moment(dateFromDatabase, 'ddd MMM DD YYYY HH:mm:ss GMT Z').diff(Date.now(), 'hours');
```
## Moment Format
```js
moment(data.appointment_time, ["HH:mm:SS"]).format("hh:mmA");
```
## Disable Date for Date Picker
```js
const todisabledDate = (value) => {
    let yes = moment().subtract(1, "days");
    return value < yes;
  };
```
## 
