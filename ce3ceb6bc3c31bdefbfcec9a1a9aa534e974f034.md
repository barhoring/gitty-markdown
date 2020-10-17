# Index Routes

Rather than show a blank page at /invoices, let’s add an Index Route. Index Routes are just another child of a route, except their path is /. An Index Route will render when no other sibling matches the location.

First create a new component:

```javascript
const InvoicesIndex = () => (
  <div>
    <p>Maybe put some pretty graphs here or something.</p>
  </div>
);
```

Next, add it as a child of <Invoices> with a path of /.

```javascript
<Router>
  <Invoices path="invoices">
    <InvoicesIndex path="/" />
    <Invoice path=":invoiceId" />
  </Invoices>
  {/*...*/}
</Router>
```

Now click on the “invoices” link. When you visit “/invoices” you’ll see the new component.
