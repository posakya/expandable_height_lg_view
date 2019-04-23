# expandable_height_lg_view
Step 1 : Add the JitPack repository to your build file

Add it in your root build.gradle at the end of repositories

       allprojects {
		      repositories {
			      ...
			    maven { url 'https://www.jitpack.io' }
		    }
	    }

Step 2 : Add the dependency

      dependencies {
	        implementation 'com.github.posakya:expandable_height_lg_view:0.1'
	    }
      
Step 3 : Call it on xml layout

          <ScrollView
              xmlns:android="http://schemas.android.com/apk/res/android"
              android:layout_width="match_parent"
              android:layout_height="match_parent">

              /*

              for expandable height list view
	    
	      */
                       <com.ar_tech.expandable_height_lg_view.ExpandableHeightListView
                          android:layout_width="match_parent"
                          android:layout_height="wrap_content"
                          android:id="@+id/lv">
                      </com.ar_tech.expandable_height_lg_view.ExpandableHeightListView>

 	      /*

              for expandable height grid view
	    
	      */
                      <com.ar_tech.expandable_height_lg_view.ExpandableHeightGridView
                          android:layout_width="match_parent"
                          android:layout_height="wrap_content"
                          android:id="@+id/gv">
                      </com.ar_tech.expandable_height_lg_view.ExpandableHeightGridView>

              </ScrollView>
              
 Step 4 : In activity or fragment
 
           //ListView
          ExpandableHeightListView listView = findViewById(R.id.lv);
          listView.setAdapter(adapter);
          listView.setExpanded(true);

          //GridView
          ExpandableHeightGridView gridView = findViewById(R.id.gv);
          gridView.setNumColumns(4);
          gridView.setAdapter(adapter);
          gridView.setExpanded(true);
