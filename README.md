# topup-alert-dialouge
this is flutter code for alert dialouge message

import 'package:flutter/material.dart';

void main() => runApp(MaterialApp(
      home: App2(),
    ));

class App2 extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text("Popup alert dialogue"),
      ),
      body: Center(
        child: ElevatedButton(
          child: Text("Click Me"),
          onPressed: () {
            showDialog(
                context: context,
                builder: (context) {
                  return AlertDialog(
                    content: Container(
                      child: Column(
                        children: <Widget>[
                          Container(
                            padding: EdgeInsets.all(10.0),
                            margin: EdgeInsets.all(10.0),
                            child: Image.asset("img/pic.png"),
                          ),
                          Container(
                            padding: EdgeInsets.all(10.0),
                            child: Text("Hurrah!"),
                          ),
                          Container(
                            padding: EdgeInsets.all(10.0),
                            child: Text(
                              "Top-up Successfully Done",
                              style:
                                  TextStyle(fontSize: 20.0, color: Colors.blue),
                            ),
                          ),
                          Container(
                            child: Text("You Earned 2 Points"),
                          ),
                          Container(
                            padding: EdgeInsets.all(20.0),
                            margin: EdgeInsets.all(40.0),
                            child: Column(
                              children: <Widget>[
                                ElevatedButton(
                                    onPressed: () {},
                                    child: Text(
                                      "BACK TO HOME",
                                      style: TextStyle(fontSize: 15.0),
                                    )),
                              ],
                            ),
                          ),
                          Container(
                            padding: EdgeInsets.all(5.0),
                              child: Text("Save Transaction Record"),

                          )
                        ],
                      ),
                    ),
                  );
                });
          },
        ),
      ),
    );
  }
}
