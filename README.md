import 'package:flutter/material.dart';

const Color darkBlue = Color.fromARGB(255, 18, 32, 47);

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      theme: ThemeData.dark().copyWith(
        scaffoldBackgroundColor: darkBlue,
      ),
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        body: Center(
          child: MyWidget(),
        ),
      ),
    );
  }
}

class MyWidget extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Card(
        color: Colors.white,
        elevation: 5,
        child: Container(
            width: 200,
            height: 450,
            child: Column(children: [
              Image.network(
                  'https://m.media-amazon.com/images/I/81k78iqhzoL._AC_SL1500_.jpg'),
              const Divider(color: Colors.grey),
              Row(mainAxisAlignment: MainAxisAlignment.spaceBetween, children: [
                Column(children: const [
                  const Text('Comida de gato',
                    style: TextStyle(
                      color: Colors.pink,
                    )),
                Text('Comida de gato',
                    style: TextStyle(
                      color: Colors.pink,
                    )),
              ]),
              Icon(
                Icons.people,
                color: Colors.pink,
                size: 30.0,
              )
                ])
            ])));
  }
}
