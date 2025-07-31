program tik tok

import 'package:flutter/material.dart';
import 'package:video_player/video_player.dart';

void main() => runApp(MyTikTokClone());

class MyTikTokClone extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: TikTokFeed(),
      debugShowCheckedModeBanner: false,
    );
  }
}

class TikTokFeed extends StatefulWidget {
  @override
  _TikTokFeedState createState() => _TikTokFeedState();
}

class _TikTokFeedState extends State<TikTokFeed> {
  final List<String> videoUrls = [
    'https://sample-videos.com/video123/mp4/720/big_buck_bunny_720p_1mb.mp4',
    'https://sample-videos.com/video123/mp4/720/big_buck_bunny_720p_1mb.mp4'
  ];

  @override
  Widget build(BuildContext context) {
    return PageView.builder(
      scrollDirection: Axis.vertical,
      itemCount: videoUrls.length,
      itemBuilder: (context, index) {
        return VideoPlayerItem(videoUrl: videoUrls[index]);
      },
    );
  }
}

class
