# navigationBar
iOS 导航渐变，并保持状态
- (void)scrollViewDidScroll:(UIScrollView *)scrollView{
    alpha = scrollView.contentOffset.y/600;
    if (alpha > 1) {
        alpha = 1;
    }
    if (scrollView == _tab) {
        [self bgView].backgroundColor = [UIColor colorWithRed:0.2 green:0.5 blue:0.7 alpha:alpha];
    }
}
