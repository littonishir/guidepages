# guidepages

## 1.布局文件中加入自定义的FrameLayout

```xml
    <com.littonishir.guidepages.PageFrameLayout
        android:id="@+id/contentFrameLayout"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />
```

## 2.设置资源文件及

```java
public class MainActivity extends AppCompatActivity {

    private PageFrameLayout contentFrameLayout;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        contentFrameLayout = findViewById(R.id.contentFrameLayout);
        // 设置资源文件及zhishiqi选中圆点
        contentFrameLayout.setUpViews(new int[]{
                R.layout.page_tab1,
                R.layout.page_tab2,
                R.layout.page_tab3,
                R.layout.page_tab4
        }, R.drawable.guide_on, R.drawable.guide_off,this);

    }
}
```