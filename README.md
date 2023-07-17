import 'package:flutter/material.dart';

void main() {
  runApp(LoginApp());
}

class LoginApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: LoginPage(),
    );
  }
}

class LoginPage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Login Page'),
      ),
      body: Container(
        padding: EdgeInsets.all(16.0),
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: [
            Image.asset('assets/login_image.png'),
            SizedBox(height: 16.0),
            TextField(
              decoration: InputDecoration(
                hintText: 'Username',
              ),
            ),
            SizedBox(height: 8.0),
            TextField(
              decoration: InputDecoration(
                hintText: 'Password',
              ),
              obscureText: true,
            ),
            SizedBox(height: 16.0),
            RaisedButton(
              onPressed: () {
                // Login button pressed
              },
              child: Text('Login'),
            ),
          ],
        ),
      ),
    );
  }
}

class Event {
  final String title;
  final String description;
  final DateTime date;

  Event({required this.title, required this.description, required this.date});
}

final List<Event> events = [
  Event(
    title: 'Event 1',
    description: 'Description for Event 1',
    date: DateTime(2023, 7, 18),
  ),
  Event(
    title: 'Event 2',
    description: 'Description for Event 2',
    date: DateTime(2023, 7, 19),
  ),
  Event(
    title: 'Event 3',
    description: 'Description for Event 3',
    date: DateTime(2023, 7, 20),
  ),
];


flutter:
  fonts:
    - family: CustomFont
      fonts:
        - asset: fonts/CustomFont-Regular.ttf
        - asset: fonts/CustomFont-Bold.ttf
          weight: 700


TextStyle(
  fontFamily: 'CustomFont',
  fontWeight: FontWeight.bold,
  fontSize: 18.0,
),
