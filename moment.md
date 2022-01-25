## To Find different between two timestamps
```
const timestamp = moment(dateFromDatabase, 'ddd MMM DD YYYY HH:mm:ss GMT Z').diff(Date.now(), 'hours');
```
## Moment Format
```
moment(data.appointment_time, ["HH:mm:SS"]).format("hh:mmA");
```
## Disable Date for Date Picker
```
const todisabledDate = (value) => {
    let yes = moment().subtract(1, "days");
    return value < yes;
  };
```
## 
