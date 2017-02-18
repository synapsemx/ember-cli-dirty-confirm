#ember-cli-dirty-confirm

A dirty model route transition aborter. It will show a confirm dialog giving you a chance to cancel a route change. If you agree, it will rollback your model.

##Usage

```
ember install synapsemx/ember-cli-dirty-confirm
```

```js
import DirtyConfirmRouteMixin from 'ember-cli-dirty-confirm/mixins/dirty-confirm-route';

export default Ember.Route.extend(DirtyConfirmRouteMixin, {
  // optional, the default message is "Leaving without saving will cancel your changes. Are you sure?"
  dirtyMessage: "You forgot to save!",
  // optional, temporarily disable the message
  isDirtyConfirmEnabled: false
});
```

It also exposes an action called `toggleDirtyConfirm`, so you can toggle off from outside the route.
