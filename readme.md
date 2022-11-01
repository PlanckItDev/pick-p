# PICK-P

Current Version **0.0.1**

PICK-P is the PI-FALC Communication Kit - Protocol

See PI-FALC for the Full Application Life Cycle.

## Planck It Communication Kit - Protocol

PICK-P provides a standard way of communication within a Full Application Life Cycle to develop modern Applications.

### Goal

Standard specification for Communication within the Development Process of modern Applications.

-> Tracability
-> Maintainability
-> Action and Reaction

Within the FALC a Stakeholder is the Root-Source of an Event by changing the planned base.

When an event is recorded a reaction will follow in some kind.

### Global Fields

- **version:**
  To indicate the used PICK-P version

#### Plan

### Create

#### Workflow

```{include} ./src/schema/schema.json

```

### Configure

```javascript

```

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
