
```jsx
import React from 'react';
import ReactPhoneInput from 'mui-phone-input';
import { TextField } from '@mui/material';

function PhoneField(props) {
  const { value, defaultCountry, onChange } = props;

  return (
    <React.Fragment>
      {/* Simple usage */}
      <ReactPhoneInput
        value={value}
        onChange={onChange} // passed function receives the phone value
        component={TextField}
      />

      {/* Configure more */}
      <ReactPhoneInput
        value={value}
        defaultCountry={defaultCountry || 'gb'}
        onChange={onChange}
        component={TextField}
        inputProps={{
          sx: {
            margin: '10px 0',
          },
        }}
        dropdownStyle={{
          fontFamily: 'sans-serif',
        }}
      />
    </React.Fragment>
  );
}

export default PhoneField;
```