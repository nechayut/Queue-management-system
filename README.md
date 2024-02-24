# Queue-management-system
Queue management system with google sheet by using Apps Script : 
https://docs.google.com/spreadsheets/d/1QhQrbEDKYTZf5wqOwADd4N0Je3fQJt1SlZBcspDA7Ck/edit#gid=0

Apps Script Code

function getroomfinal() {
  var ss = SpreadsheetApp.getActiveSpreadsheet();
  var sheet = ss.getSheetByName("register");
  var room1 = ss.getSheetByName("ห้อง 1");
  var room2 = ss.getSheetByName("ห้อง 2");
  var room3 = ss.getSheetByName("ห้อง 3");
  var room4 = ss.getSheetByName("ห้อง 4");
  var room5 = ss.getSheetByName("ห้อง 5");

  for(var x = 4;x < 9;x++){
    if((sheet.getRange(x,4).getValue()) == "Done"){
        for(var i = 13;i<321;i++){
          if((sheet.getRange(i,5).getValue()) == ""){

            if (sheet.getRange(x,2).getValue() == "ห้อง 1"){
              sheet.getRange(i,5).setValue(sheet.getRange(x,2).getValue())
              for(var y = 4;y<100;y++){
                if((room1.getRange(y,9).getValue()) == ""){
                  room1.getRange(y,9).setValue("Waiting")
                  break;
                }
              } break;
            } else if (sheet.getRange(x,2).getValue() == "ห้อง 2"){
              sheet.getRange(i,5).setValue(sheet.getRange(x,2).getValue())
              for(var y = 4;y<100;y++){
                if((room2.getRange(y,9).getValue()) == ""){
                  room2.getRange(y,9).setValue("Waiting")
                  break;
                }
              } break;
            } else if (sheet.getRange(x,2).getValue() == "ห้อง 3"){
              sheet.getRange(i,5).setValue(sheet.getRange(x,2).getValue())
              for(var y = 4;y<100;y++){
                if((room3.getRange(y,9).getValue()) == ""){
                  room3.getRange(y,9).setValue("Waiting")
                  break;
                }
              } break;
            } else if (sheet.getRange(x,2).getValue() == "ห้อง 4"){
              sheet.getRange(i,5).setValue(sheet.getRange(x,2).getValue())
              for(var y = 4;y<100;y++){
                if((room4.getRange(y,9).getValue()) == ""){
                  room4.getRange(y,9).setValue("Waiting")
                  break;
                }
              } break;
            } else if (sheet.getRange(x,2).getValue() == "ห้อง 5"){
              sheet.getRange(i,5).setValue(sheet.getRange(x,2).getValue())
              for(var y = 4;y<100;y++){
                if((room5.getRange(y,9).getValue()) == ""){
                  room5.getRange(y,9).setValue("Waiting")
                  break;
                }
              } break;
            }
          }
        } break;
    }
  }
}  
