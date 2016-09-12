单行滚动collectionView，滚动最后的item居中，可每次滚动一个item，也可多个
关键代码如下
- (void) scrollViewWillEndDragging:(UIScrollView *)scrollView withVelocity:(CGPoint)velocity targetContentOffset:(inout CGPoint *)targetContentOffset {
    
    CGFloat offSetX = targetContentOffset->x; //偏移量
    //    CGFloat offSetX = scrollView.contentOffset.x; //当前偏移量   仅仅滑动一个单元格

    CGFloat itemWidth = SCREEN_WIDTH-100;   //itemSizem 的宽
    
    
    //itemSizem的宽度+行间距 = 页码的宽度
    
    NSInteger pageWidth = itemWidth + 15;
    
    //根据偏移量计算 第几页
    
    NSInteger pageNum = (offSetX+pageWidth/2)/pageWidth;
    
    //根据显示的第几页,从而改变偏移量
    
    targetContentOffset->x = pageNum*pageWidth;
    
    NSLog(@"%.1f  page %zd",targetContentOffset->x, pageNum);
    
}
