### numeric string
```ts
type NumericString = `${number}`

const a: NumericString = '100'
const b: NumericString = '2e24'
const c: NumericString = '365.25'
```

### template literal types
```ts
type Dates = 'Year' | 'Month' | 'Day' | 'Hour' | 'Minute' | 'Second';

type DatesAnyCase = Dates | Uppercase<Dates> | Lowercase<Dates>;
// Dates | "YEAR" | "MONTH" | "DAY" | "HOUR" | "MINUTE" | "SECOND" | "year" | "month" | "day" | "hour" | "minute" | "second"

type DatesStringValue =
  | `${number}`
  | `${number}${DatesAnyCase}`
  | `${number} ${DatesAnyCase}`;
// `${number}` | `${number}Year` | `${number}Month` | `${number}Day` | `${number}Hour` | `${number}Minute` | `${number}Second` | `${number}YEAR` | `${number}MONTH` | `${number}DAY` | `${number}HOUR` | `${number}MINUTE` | `${number}SECOND` | `${number}year` | `${number}month` | `${number}day` | `${number}hour` | `${number}minute` | `${number}second` | `${number} Year` | `${number} Month` | `${number} Day` | `${number} Hour` | `${number} Minute` | `${number} Second` | `${number} YEAR` | `${number} MONTH` | `${number} DAY` | `${number} HOUR` | `${number} MINUTE` | `${number} SECOND` | `${number} year` | `${number} month` | `${number} day` | `${number} hour` | `${number} minute` | `${number} second`

const a: DatesStringValue = '1Month';
const b: DatesStringValue = '142 Day';
const c: DatesStringValue = '42';
```