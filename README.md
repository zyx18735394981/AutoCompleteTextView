# AutoCompleteTextView
搜索框_自动填充
                    
                      
        <AutoCompleteTextView
        android:id="@+id/auto"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:completionThreshold="1"
        android:completionHint="请输入所查信息"
        android:layout_below="@id/mt"
        android:layout_margin="20dp"

        />
        
        
        
        package com.zyx.paomadeng_textview_12_6;

        import android.os.Bundle;
        import android.support.v7.app.ActionBarActivity;
        import android.widget.ArrayAdapter;
        import android.widget.AutoCompleteTextView;


        public class MainActivity extends ActionBarActivity {
            private  AutoCompleteTextView auto;
            private String[] s;

            @Override
            protected void onCreate(Bundle savedInstanceState) {
                super.onCreate(savedInstanceState);
                setContentView(R.layout.activity_main);
                s=new String[]{"aaa","bbb","ccc","abb","acc","bdd","bvv"};


              auto=(AutoCompleteTextView) findViewById(R.id.auto);

                ArrayAdapter<String> adapter=new ArrayAdapter<String>(this,android.R.layout.simple_spinner_dropdown_item,s);

                auto.setAdapter(adapter);
            }



        }
