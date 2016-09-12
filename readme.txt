{\rtf1\ansi\ansicpg936\cocoartf1404\cocoasubrtf470
{\fonttbl\f0\fnil\fcharset134 PingFangSC-Regular;\f1\fswiss\fcharset0 Helvetica;\f2\fnil\fcharset0 Menlo-Regular;
}
{\colortbl;\red255\green255\blue255;\red170\green13\blue145;\red92\green38\blue153;\red0\green116\blue0;
\red100\green56\blue32;\red28\green0\blue207;\red46\green13\blue110;\red196\green26\blue22;}
\paperw11900\paperh16840\margl1440\margr1440\vieww10800\viewh8400\viewkind0
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0

\f0\fs24 \cf0 \'b5\'a5\'d0\'d0\'b9\'f6\'b6\'af
\f1 collectionView
\f0 \'a3\'ac\'b9\'f6\'b6\'af\'d7\'ee\'ba\'f3\'b5\'c4
\f1 item
\f0 \'be\'d3\'d6\'d0\'a3\'ac\'bf\'c9\'c3\'bf\'b4\'ce\'b9\'f6\'b6\'af\'d2\'bb\'b8\'f6item\'a3\'ac\'d2\'b2\'bf\'c9\'b6\'e0\'b8\'f6\
\'b9\'d8\'bc\'fc\'b4\'fa\'c2\'eb\'c8\'e7\'cf\'c2\
\pard\tx529\pardeftab529\pardirnatural\partightenfactor0

\f2\fs22 \cf0 \CocoaLigature0 - (\cf2 void\cf0 ) scrollViewWillEndDragging:(\cf3 UIScrollView\cf0  *)scrollView withVelocity:(\cf3 CGPoint\cf0 )velocity targetContentOffset:(\cf2 inout\cf0  \cf3 CGPoint\cf0  *)targetContentOffset \{\
    \
    \cf3 CGFloat\cf0  offSetX = targetContentOffset->\cf3 x\cf0 ; \cf4 //
\f0 \'c6\'ab\'d2\'c6\'c1\'bf
\f2 \cf0 \
\cf4 //    CGFloat offSetX = scrollView.contentOffset.x; //
\f0 \'b5\'b1\'c7\'b0\'c6\'ab\'d2\'c6\'c1\'bf
\f2    
\f0 \'bd\'f6\'bd\'f6\'bb\'ac\'b6\'af\'d2\'bb\'b8\'f6\'b5\'a5\'d4\'aa\'b8\'f1
\f2 \cf0 \
\
    \cf3 CGFloat\cf0  itemWidth = \cf5 SCREEN_WIDTH\cf0 -\cf6 100\cf0 ;   \cf4 //itemSizem 
\f0 \'b5\'c4\'bf\'ed
\f2 \cf0 \
    \
    \
    \cf4 //itemSizem
\f0 \'b5\'c4\'bf\'ed\'b6\'c8
\f2 +
\f0 \'d0\'d0\'bc\'e4\'be\'e0
\f2  = 
\f0 \'d2\'b3\'c2\'eb\'b5\'c4\'bf\'ed\'b6\'c8
\f2 \cf0 \
    \
    \cf3 NSInteger\cf0  pageWidth = itemWidth + \cf6 15\cf0 ;\
    \
    \cf4 //
\f0 \'b8\'f9\'be\'dd\'c6\'ab\'d2\'c6\'c1\'bf\'bc\'c6\'cb\'e3
\f2  
\f0 \'b5\'da\'bc\'b8\'d2\'b3
\f2 \cf0 \
    \
    \cf3 NSInteger\cf0  pageNum = (offSetX+pageWidth/\cf6 2\cf0 )/pageWidth;\
    \
    \cf4 //
\f0 \'b8\'f9\'be\'dd\'cf\'d4\'ca\'be\'b5\'c4\'b5\'da\'bc\'b8\'d2\'b3
\f2 ,
\f0 \'b4\'d3\'b6\'f8\'b8\'c4\'b1\'e4\'c6\'ab\'d2\'c6\'c1\'bf
\f2 \cf0 \
    \
    targetContentOffset->\cf3 x\cf0  = pageNum*pageWidth;\
    \
    \cf7 NSLog\cf0 (\cf8 @"%.1f  page %zd"\cf0 ,targetContentOffset->\cf3 x\cf0 , pageNum);\
    \
\}\
}