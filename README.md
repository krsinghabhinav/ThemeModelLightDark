# ThemeModelLightDark

import 'package:flutter/material.dart';
import 'package:google_fonts/google_fonts.dart';

class myTheme {
  static ThemeData lightTheme(BuildContext context) => ThemeData(
        primarySwatch: Colors.blue,
        canvasColor: Colors.white,
        fontFamily: GoogleFonts.poppins().fontFamily,
        cardColor: Colors.white,
        colorScheme: ColorScheme(
          brightness: Brightness.light,
          primary: Colors.black,
          onPrimary: Colors.white,
          secondary: Colors.black87,
          onSecondary: Colors.black,
          error: Colors.red,
          onError: Colors.red,
          surface: const Color.fromARGB(255, 255, 255, 255),
          onSurface: Colors.black,
        ),
        appBarTheme: AppBarTheme(
          backgroundColor: Colors.white,
          elevation: 0,
          iconTheme: IconThemeData(color: Colors.black),
        ),
        floatingActionButtonTheme: FloatingActionButtonThemeData(
          backgroundColor: Colors.black,
        ),
      );

  static ThemeData darkTheme(BuildContext context) => ThemeData(
        canvasColor: Colors.black,
        fontFamily: GoogleFonts.poppins().fontFamily,
        cardColor: const Color.fromARGB(255, 0, 0, 0),
        colorScheme: ColorScheme(
          brightness: Brightness.dark,
          primary: Colors.black,
          onPrimary: Colors.black,
          secondary: Colors.grey[300]!,
          onSecondary: Colors.black,
          error: Colors.red,
          onError: Colors.red,
          surface: const Color.fromARGB(255, 0, 0, 0)!,
          onSurface: Colors.white,
        ),
        appBarTheme: AppBarTheme(
          backgroundColor: Colors.black,
          elevation: 0,
          iconTheme: IconThemeData(color: Colors.white),
        ),
        floatingActionButtonTheme: FloatingActionButtonThemeData(
          backgroundColor: Colors.white,
        ),
      );
}

=============================================================================



mainfile===


import 'package:apibasedproject/view/welcomePage/welcomePage.dart';
import 'package:apibasedproject/widgets/theme/mytheme.dart';
import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  // This widget is the root of your application.
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      themeMode: ThemeMode.system,
      theme: myTheme.lightTheme(context),
      darkTheme: myTheme.darkTheme(context),
      home: Welcomepage(),
    );
  }
}
