# 日历组件

### 注意

采用三方组件clndr，文档：[http://github.com/kylestetz/CLNDR](http://github.com/kylestetz/CLNDR)

### 主要参数说明
```js
$('.parent-element').clndr({
	// The template: this could be stored in markup as a
    //   <script type="text/template"></script>
    // or pulled in as a string
    template: clndrTemplate,
    // Click callbacks! The keyword 'this' is set to the clndr instance in all
    // callbacks.
    clickEvents: {
        // Fired whenever a calendar box is clicked. Returns a 'target' object
        // containing the DOM element, any events, and the date as a moment.js
        // object.
        click: function (target) {...},

        // Fired when a user goes to the current month and year. Returns a
        // moment.js object set to the correct month.
        today: function (month) {...},

        // Fired when a user goes forward a month. Returns a moment.js object
        // set to the correct month.
        nextMonth: function (month) {...},

        // Fired when a user goes back a month. Returns a moment.js object set
        // to the correct month.
        previousMonth: function (month) {...},

        // Fires any time the month changes as a result of a click action.
        // Returns a moment.js object set to the correct month.
        onMonthChange: function (month) {...},

        // Fired when the next year button is clicked. Returns a moment.js
        // object set to the correct month and year.
        nextYear: function (month) {...},

        // Fired when the previous year button is clicked. Returns a moment.js
        // object set to the correct month and year.
        previousYear: function (month) {...},

        // Fires any time the year changes as a result of a click action. If
        // onMonthChange is also set, it is fired BEFORE onYearChange. Returns
        // a moment.js object set to the correct month and year.
        onYearChange: function (month) {...},

        // Fired when a user goes forward a period. Returns moment.js objects
        // for the updated start and end date.
        nextInterval: function (start, end) {...},

        // Fired when a user goes back an interval. Returns moment.js objects for
        // the updated start and end date.
        previousInterval: function (start, end) {...},

        // Fired whenever the time period changes as configured in lengthOfTime.
        // Returns moment.js objects for the updated start and end date.
        onIntervalChange: function (start, end) {...}
    },
    // An array of event objects
    events: []
});
```


## 示例

<iframe width="100%" height="700" src="//jsrun.net/9FpKp/embedded/all/light/" allowfullscreen="allowfullscreen" frameborder="0"></iframe>
