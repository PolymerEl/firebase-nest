[![Build Status](https://travis-ci.org/PolymerEl/firebase-nest.svg?branch=master)](https://travis-ci.org/PolymerEl/firebase-nest)
[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://beta.webcomponents.org/element/polymerEl/firebase-nest)

# \<firebase-nest\>


polymerfire based util to construct firebase nested and lookup datastructure


Example Usage:

This example will add `{"code": {value of country code retrieved from firebase}}` to each array Element at `/countryList`
```html
	<firebase-app  auth-domain="pre-ignition-meta.firebaseapp.com" database-url="https://pre-ignition-meta.firebaseio.com/" api-key="AIzaSyAbLJ5nMHaFS_YXioay8b28RnV43JvoEms">
  </firebase-app>
  <firebase-nest id="nest" log path="/countryList" data="{{data}}">
    <template is="dom-repeat" items="[[data]]">
      <p>item: [[item.$key]]</p>
      <firebase-value id="value" log key="code" data="[[item]]" path="/countryNames/[[item.$key]]/country-code"></firebase-value>
    </template>
  </firebase-nest>

```
