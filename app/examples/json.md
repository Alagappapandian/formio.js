---
title: JSON Powered
layout: vtabs
section: examples
weight: 30
---
### JSON Powered Forms
All forms that are rendered within this framework are JSON powered forms.

```html
<link rel="stylesheet" href="https://unpkg.com/formiojs@latest/dist/formio.full.min.css">
<script src="https://unpkg.com/formiojs@latest/dist/formio.full.min.js"></script>
<div id="formio"></div>
```

<div class="row">
<div class="col col-sm-6">

<pre>
Formio.createForm(document.getElementById('formio'), {
  components: [
    {
      type: 'textfield',
      key: 'firstName',
      label: 'First Name',
      placeholder: 'Enter your first name.',
      input: true
    },
    {
      type: 'textfield',
      key: 'lastName',
      label: 'Last Name',
      placeholder: 'Enter your last name',
      input: true
    },
    {
      type: 'select',
      key: 'select',
      label: 'Favorite Color',
      placeholder: 'Select your favorite color',
      template: '<span>{% raw %}{{ item.label }}{% endraw %}</span>',
      multiple: true,
      dataSrc: 'values',
      input: true,
      valueProperty: '',
      defaultValue: '',
      filter: '',
      refreshOn: '',
      data: {
        custom: '',
        resource: '',
        url: '',
        json: '',
        values: [
          {
            label: 'Red',
            value: 'red'
          },
          {
            label: 'Blue',
            value: 'blue'
          },
          {
            label: 'Green',
            value: 'green'
          },
          {
            label: 'Yellow',
            value: 'yellow'
          },
          {
            label: 'Purple',
            value: 'purple'
          },
          {
            label: 'Orange',
            value: 'orange'
          },
          {
            label: 'Black',
            value: 'black'
          }
        ]
      }
    },
    {
      type: 'address',
      key: 'address',
      label: 'Address',
      placeholder: 'Enter your address',
      input: true,
      map: {
          region: '',
          key: ''
      }
    },
    {
      type: 'day',
      key: 'birthdate',
      label: 'Birthdate',
      input: true,
      dayFirst: false,
      fields: {
        year: {
          required: false,
          placeholder: '',
          type: 'text'
        },
        month: {
          required: false,
          placeholder: '',
          type: 'select'
        },
        day: {
          required: false,
          placeholder: '',
          type: 'text'
        }
      },
    },
    {
      type: 'button',
      action: 'submit',
      label: 'Submit',
      theme: 'primary'
    }
  ]
});
</pre>

</div>
<div class="col col-sm-6">
<h3>Result</h3>
<div class="well">
<div id="formio"></div>
<script type="text/javascript">
Formio.createForm(document.getElementById('formio'), {
  components: [
    {
      type: 'textfield',
      key: 'firstName',
      label: 'First Name',
      placeholder: 'Enter your first name.',
      input: true
    },
    {
      type: 'textfield',
      key: 'lastName',
      label: 'Last Name',
      placeholder: 'Enter your last name',
      input: true
    },
    {
      type: 'select',
      key: 'select',
      label: 'Favorite Color',
      placeholder: 'Select your favorite color',
      template: '<span>{% raw %}{{ item.label }}{% endraw %}</span>',
      multiple: true,
      dataSrc: 'values',
      input: true,
      valueProperty: '',
      defaultValue: '',
      filter: '',
      refreshOn: '',
      data: {
        custom: '',
        resource: '',
        url: '',
        json: '',
        values: [
          {
            label: 'Red',
            value: 'red'
          },
          {
            label: 'Blue',
            value: 'blue'
          },
          {
            label: 'Green',
            value: 'green'
          },
          {
            label: 'Yellow',
            value: 'yellow'
          },
          {
            label: 'Purple',
            value: 'purple'
          },
          {
            label: 'Orange',
            value: 'orange'
          },
          {
            label: 'Black',
            value: 'black'
          }
        ]
      }
    },
    {
      type: 'address',
      key: 'address',
      label: 'Address',
      placeholder: 'Enter your address',
      input: true,
      map: {
          region: '',
          key: ''
      }
    },
    {
      type: 'day',
      key: 'birthdate',
      label: 'Birthdate',
      input: true,
      dayFirst: false,
      fields: {
        year: {
          required: false,
          placeholder: '',
          type: 'text'
        },
        month: {
          required: false,
          placeholder: '',
          type: 'select'
        },
        day: {
          required: false,
          placeholder: '',
          type: 'text'
        }
      },
    },
    {
      type: 'button',
      action: 'submit',
      label: 'Submit',
      theme: 'primary'
    }
  ]
});
</script>
</div>
</div>
</div>


