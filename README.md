# datetimepicker
前端时间控件

源文件为bootstrap-datetimepicker.js和bootstrap-datetimepicker.min.js.
修改后的文件为bootstrap-datetimepicker-ch.js

修改部分：
1、增加了中文部分（locales下的中文支持不符合AMD规范，requireJs加载报错）

var dates = $.fn.datetimepicker.dates = {

    en: {
      days:        ['Sunday', 'Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday', 'Sunday'],
      daysShort:   ['Sun', 'Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun'],
      daysMin:     ['Su', 'Mo', 'Tu', 'We', 'Th', 'Fr', 'Sa', 'Su'],
      months:      ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December'],
      monthsShort: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'],
      meridiem:    ['am', 'pm'],
      suffix:      ['st', 'nd', 'rd', 'th'],
      today:       'Today',
      clear:       'Clear'
    },
    cn: {
      days:        ['星期日', '星期一', '星期二', '星期三', '星期四', '星期五', '星期六', '星期日'],
      daysShort:   ['星期日', '星期一', '星期二', '星期三', '星期四', '星期五', '星期六', '星期日'],
      daysMin:     ['日', '一', '二', '三', '四', '五', '六', '日'],
      months:      ['1', '2', '3', '4', '5', '6', '7', '8', '9', '10', '11', '12'],
      monthsShort: ['一月', '二月', '三月', '四月', '五月', '六月', '七月', '八月', '九月', '十月', '十一月', '十二月'],
      meridiem:    ['上午', '下午'],
      suffix:      ['st', 'nd', 'rd', 'th'],
      today:       '今天'
    }
    
  };
  
2、修改了Firefox下的错误

//this.defaultTimeZone = (new Date).toString().split('(')[1].slice(0, -1);

  this.defaultTimeZone='GMT '+(new Date()).getTimezoneOffset()/60;
