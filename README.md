# data
 css
//     program 9

//     Write a JavaScript function to get the last day of a month.   

// Test Data :
// console.log(lastday(2014,0));
// console.log(lastday(2014,1));
// console.log(lastday(2014,11));
// Output :
// 31
// 28
// 31

var date_diff_indays = function(date1, date2) {
    dt1 = new Date(date1);
    dt2 = new Date(date2);
    return Math.floor((Date.UTC(dt2.getFullYear(), dt2.getMonth(), dt2.getDate()) - Date.UTC(dt1.getFullYear(), dt1.getMonth(), dt1.getDate()) ) /(1000 * 60 * 60 * 24));
    }
    console.log(date_diff_indays('04/02/2014', '11/04/2014'));
    console.log(date_diff_indays('12/02/2014', '11/04/2014'));
    

//     progrm 10

//     Write a JavaScript function to calculate 'yesterday day'.   

// Test Data :
// console.log(yesterday('Nov 15, 2014'));
// console.log(yesterday('Nov 16, 2015'));
// console.log(yesterday('Nov 17, 2016'));
// Output :
// "Fri Nov 14 2014 00:00:00 GMT+0530 (India Standard Time)"
// "Sun Nov 15 2015 00:00:00 GMT+0530 (India Standard Time)"
// "Wed Nov 16 2016 00:00:00 GMT+0530 (India Standard Time)"

var yesterday =  function(date1){
    var dt = new Date(date1);
  return new Date((dt.setDate(dt.getDate()-1))).toString();
}
console.log(yesterday('Nov 15, 2014'));
console.log(yesterday('Nov 16, 2015'));
console.log(yesterday('Nov 17, 2016'));


// program11

// Write a JavaScript function to get the maximum date from an array of dates. Go to the editor

// Test Data :
// console.log(max_date(['2015/02/01', '2015/02/02', '2015/01/03']));
// Output :
// "2015/02/02"

function max_date(all_dates) {
    var max_dt = all_dates[0],
      max_dtObj = new Date(all_dates[0]);
    all_dates.forEach(function(dt, index)
      {
      if ( new Date( dt ) > max_dtObj)
      {
      max_dt = dt;
      max_dtObj = new Date(dt);
      }
      });
     return max_dt;
      }
    console.log(max_date(['2015/02/01', '2015/02/02', '2015/01/03']));
    


// program 12
// Write a JavaScript function to get the minimum date from an array of dates. Go to the editor

// Test Data :
// console.log(min_date(['2015/02/01', '2015/02/02', '2015/01/03']));
// Output :
// "2015/01/03"

function min_date(all_dates) {
    var min_dt = all_dates[0],
     min_dtObj = new Date(all_dates[0]);
    all_dates.forEach(function(dt, index)
     {
     if ( new Date( dt ) < min_dtObj)
     {
     min_dt = dt;
     min_dtObj = new Date(dt);
     }
     });
    return min_dt;
     }
   console.log(min_date(['2015/02/01', '2015/02/02', '2015/01/03']));
