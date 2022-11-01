# PICK-P

## Planck It Communication Kit - Protocol

Global Fields:

- version
  To indicate the used PICK-P version

### Plan

### Create

#### Workflow

```javascript
const a = {};
```

### Configure

### Verify

```javascript
{
  test: [
    {
      path: 'Test File Path',
      name: 'Test Description',
      uut: {
        name: 'Unit under Test' | ['Unit under Test 1', ...['Unit under Test N']],
        path: 'Unit under Test Path' | ['Unit under Test Path 1', ...['Unit under Test Path N']]
      },
      group: {
        name: 'Group Name',
        path: 'Group Path'
      },
      status: [{
        type: 'skipped' | 'failed' | 'success',
        reason: [
          {
            comment: 'Skipped comment',
          },
          {
            assertion: [{
              line: 'lineNumber',
              column: 'columnNumber',
              expected: ['arg 1', 'arg N'],
              received: ['arg'],
            }],
            trace: [{
              path: 'filePath',
              line: 'lineNumber',
              column: 'columnNumber',
            }]
          }
        ]
      }], // OneOf
      type: ['positive', 'negative'], // OneOf
    }
  ],
  group: [{
    name: 'Group Name',
    path: 'Group Path',
    parent: {
      name: 'Parent Name',
      path: 'Parent Path',
    }
  }]
}
```

### Secure

### Deploy

### Release

### Monitor

### Manage
