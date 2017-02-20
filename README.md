# adapt-systemInfo

This is an Adapt **authoring tool plugin** which adds a toolbar to the app window which is visible only to super users.

## Installation

1. Copy all sub-folders in `/routes/` to `/routes/` in your authoring tool folder.
2. Copy all sub-folders in `/frontend/` to `/frontend/src/plugins/` in your authoring tool folder.

## Usage

The plugin hooks into Origin's events API, and can be instantiated/controlled using the following syntax:

Adding a super toolbar instance:
```
Origin.trigger('superToolbar:add', [
  {
    title: 'Label',
    icon: 'fa-wrench', // uses font awesome
    event: 'someevent'
  }
]);
```

Handling super toolbar interaction:
```
Origin.on('superToolbar:someevent', function() {
  // do something
});
```
