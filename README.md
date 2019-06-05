# banner
banner  for viewpager
<com.hqyz.hy.banner.BannerPageview
            xmlns:banner="http://schemas.android.com/apk/res-auto"
            android:layout_width="match_parent"
            android:layout_height="182dp"
            android:id="@+id/banner"
            banner:bb_barColor="@color/black_50a"
            banner:bb_indicatorGap="5dp"
            banner:bb_textSize="14sp"
            banner:bb_textColor="@color/white"
            banner:bb_indicatorGravity="TOP"
            banner:bb_isIndicatorShow="true"
            banner:bb_indicatorSelectColor="@color/black"
            banner:bb_indicatorUnselectColor="@color/white"/>

      mBanner.setOnItemClickL(new BaseBanner.OnItemClickL() {
                @Override
                public void onItemClick(int position) {
         
                }
            });

  
  topBanner.setSource(bannerDataHelper.getBannerItems(data)).startScroll();

 private BannerDataHelper bannerDataHelper = new BannerDataHelper<BannerBean>() {
        @Override
        public BannerItem changeToBannerItem(BannerBean data) {
            BannerItem item = new BannerItem();
            item.imgUrl = data.url;
            item.title = data.text;
            return item;
        }
    };
