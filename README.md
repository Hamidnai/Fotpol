import 'package:flutter/material.dart';

void main() => runApp(FootballApp());

class FootballApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      theme: ThemeData(fontFamily: 'Arial'),
      home: MatchesPage(),
    );
  }
}

class MatchesPage extends StatelessWidget {
  final List<Map<String, String>> matches = [
    {
      'team1': 'برشلونة',
      'team2': 'ريال مدريد',
      'time': '20:00',
      'date': '25 يونيو 2025',
      'league': 'الدوري الإسباني',
    },
    {
      'team1': 'مانشستر سيتي',
      'team2': 'آرسنال',
      'time': '18:00',
      'date': '25 يونيو 2025',
      'league': 'الدوري الإنجليزي',
    },
    {
      'team1': 'الوداد',
      'team2': 'الرجاء',
      'time': '21:30',
      'date': '26 يونيو 2025',
      'league': 'الدوري المغربي',
    },
  ];

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('مباريات كرة القدم'),
        backgroundColor: Colors.green.shade800,
      ),
      body: ListView.builder(
        itemCount: matches.length,
        itemBuilder: (context, index) {
          final match = matches[index];
          return Card(
            margin: EdgeInsets.all(8),
            child: ListTile(
              leading: Icon(Icons.sports_soccer, color: Colors.green),
              title: Text('${match['team1']} vs ${match['team2']}',
                  style: TextStyle(fontWeight: FontWeight.bold)),
              subtitle: Text(
                  '${match['league']}\n🕒 ${match['time']} - ${match['date']}',
                  style: TextStyle(height: 1.5)),
            ),
          );
        },
      ),
    );
  }
}


ها هو كود تطبيق Flutter تجريبي يعرض مواعيد مباريات كرة القدم:

✅ ما يحتويه التطبيق:

قائمة مباريات مع:

أسماء الفريقين

توقيت وتاريخ المباراة

اسم البطولة


تصميم بسيط باستخدام ListView و Card لكل مباراة



---

📦 خطوات التشغيل:

1. تأكد أنك مثبت Flutter على جهازك.
(إذا لم يكن لديك Flutter: https://flutter.dev/docs/get-started/install)


2. افتح مشروع Flutter جديد وأدخل الكود في ملف lib/main.dart.


3. ثم شغّل الأمر:

flutter run




---

📲 إذا أردت لاحقاً:

ربط التطبيق بـ API حقيقيةr

إضافة إشعارات أو صفحة تفاصيل لكل مباراة

إنشاء تطبيق متكامل متعدد الصفحات


فأنا هنا لمساعدتك خطوة بخطوة.

هل تريد أن أشرح لك كيف تضيف مباراة جديدة من واجهة المستخدم أو تربطها بقاعدة بيانات؟

