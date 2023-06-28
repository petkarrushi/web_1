import 'package:flutter/material.dart';

void main(){
runApp(FlutterApp());
}

class FlutterApp extends StatelessWidget{
@override
Widget build(BuildContext context) {
return MaterialApp(
title: "FlutterApp",
debugShowCheckedModeBanner: false,
theme: ThemeData(
primarySwatch : Colors.lightGreen,
textTheme: TextTheme(
headline1:TextStyle(fontSize: 21,fontWeight: FontWeight.bold),
subtitle1: TextStyle(fontSize: 11,fontWeight: FontWeight.w500,fontStyle: FontStyle.italic),
subtitle2: TextStyle(fontSize: 11,fontWeight: FontWeight.w500,fontStyle: FontStyle.italic,color: Colors.red)
),
),
home: DashBoardScreen(),
);
}
}

class DashBoardScreen extends StatelessWidget{
@override
Widget build(BuildContext context) {
return Scaffold(
appBar: AppBar(
title: Text("Hello"),
),

        body:Column(
          children: [
            Text('Text 1',style: Theme.of(context).textTheme.headline1!.copyWith(color: Colors.orange)),
            Text('Text 2',style: Theme.of(context).textTheme.subtitle1 ),
            Text('Text 3',style:  Theme.of(context).textTheme.headline1!.copyWith(color: Colors.indigo)),
            Text('Text 4',style: Theme.of(context).textTheme.subtitle2),
          ],
        )
    );

}

}