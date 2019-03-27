<p align="center"> 
<img src="art.png">
</p>

Table of contents
=================
<!--ts-->
   * [Classes & Layouts](#classes--layouts)
   * [Layout resource IDs](#layout-resource-ids)
   * [Drawables](#drawables)
   * [Icons](#icons)
   * [Strings](#strings)
   * [Constants](#constants)
   * [Acronyms](#acronyms)
   * [MVP Package Structure](#mvp-package-structure)
   * [References](#references)
   * [Contributors](#contributors)
<!--te-->

## Classes & Layouts
| Component        | Class Name             | Layout Name                   |
| ---------------- | ---------------------- | ----------------------------- |
| Activity         | `UserProfileActivity`  | `activity_user_profile.xml`   |
| Fragment         | `SignUpFragment`       | `fragment_sign_up.xml`        |
| Dialog           | `ChangePasswordDialog` | `dialog_change_password.xml`  |
| Adapter          | `ChatAdapter`          | ---                           |
| AdapterView item | ---                    | `item_person.xml`             |
| Partial layout   | ---                    | `partial_stats_bar.xml`       |

## Layout resource IDs
| Component      | Prefix | Example                 |
| -------------- | ------ | ----------------------- |
| Button         | `btn_` | `btn_signup_dialog.xml` |
| TextView       | `tv_`  | `tv_user_status.xml`    |
| EditText       | `et_`  | `et_password.xml`       |
| ImageView      | `iv_`  | `iv_top_logo.xml`       |
| RelativeLayout | `rl_`  | `rl_root.xml`           |
| LinearLayout   | `ll_`  | `ll_root.xml`           |
| ListView       | `lv_`  | `lv_messages.xml`       |
| RecyclerView   | `rv_`  | `rv_chat.xml`           |
| Checkbox       | `chk_` | `chk_remember_me.xml`   |
| ProgressBar    | `pb_`  | `pb_upload_percent.xml` |
| RadioButton    | `rb_`  | `rb_female.xml`         |
| ToggleButton   | `tb_`  | `tb_visibility.xml`     |
| Spinner        | `spn_` | `spn_category.xml`      |
| Menu           | `mnu_` | `mnu_country.xml`       |
| GalleryView    | `gv_`  | `gv_album.xml`          |
| WebView        | `wv_`  | `wv_preview.xml`        |

## Drawables
| Asset Type   | Prefix            |		Example             |
| ------------ | ----------------- |--------------------------- |
| Action bar   | `ab_`             | `ab_stacked.9.png`         |
| Button       | `btn_`	           | `btn_send_pressed.9.png`   |
| Dialog       | `dialog_`         | `dialog_top.9.png`         |
| Divider      | `divider_`        | `divider_horizontal.9.png` |
| Icon         | `ic_`	           | `ic_star.png`              |
| Menu         | `menu_	`          | `menu_submenu_bg.9.png`    |
| Notification | `notification_`   | `notification_bg.9.png`    |
| Tabs         | `tab_`            | `tab_pressed.9.png`        |

## Icons
| Asset Type                      | Prefix           | Example                    |
| --------------------------------| ---------------- | -------------------------- |
| Icons                           | `ic_`            | `ic_star.png`              |
| Launcher icons                  | `ic_launcher`    | `ic_launcher_calendar.png` |
| Menu icons and Action Bar icons | `ic_menu`        | `ic_menu_archive.png`      |
| Status bar icons                | `ic_stat_notify` | `ic_stat_notify_msg.png`   |
| Tab icons                       | `ic_tab`         | `ic_tab_recent.png`        |
| Dialog icons                    | `ic_dialog`      | `ic_dialog_info.png`       |

## Strings
| Prefix    | Description                          |
| --------- | ------------------------------------ |
| `error_`  | An error message                     |
| `msg_`    | A regular information message        |
| `title_`  | A title, i.e. a dialog title         |
| `action_` | An action such as "Save" or "Create" |

## Constants
| Element            | Field Name Prefix |
| ------------------ | ----------------- |
| SharedPreferences  | `PREF_`           |
| Bundle             | `BUNDLE_`         |
| Fragment Arguments | `ARGUMENT_`       |
| Intent Extra       | `EXTRA_`          |
| Intent Action      | `ACTION_`         |

## Acronyms
| Good             | Bad              |
| ---------------- | ---------------- |
| `XmlHttpRequest` | `XMLHTTPRequest` |
| `getCustomerId`  | `getCustomerID`  |
| `String url`     | `String URL`     |
| `long id`        | `long ID`        |

## MVP Package Structure
```
┌─── data
│   │   Task.java (Data Model)
│   │
│   └─── source
│       │   TasksDataSource.java
│       │   TasksRepository.java
│       │
│       ├─── local
│       │       TasksDao.java
│       │       TasksLocalDataSource.java
│       │       ToDoDatabase.java
│       │
│       └─── remote
│               TasksRemoteDataSource.java
│
├─── addedittask (Action)
│       AddEditTaskActivity.java
│       AddEditTaskContract.java
│       AddEditTaskFragment.java
│       AddEditTaskPresenter.java
│
├─── taskdetail (Action)
│       TaskDetailActivity.java
│       TaskDetailContract.java
│       TaskDetailFragment.java
│       TaskDetailPresenter.java
│
├─── tasks (Action)
│       TasksActivity.java
│       TasksContract.java
│       TasksFilterType.java
│       TasksFragment.java
│       TasksPresenter.java
│
│─── util (Utility classes used in various parts of the app, e.g. for handling file access) 
│       ActivityUtils.java
│       AppExecutors.java
│       DiskIOThreadExecutor.java
│
│   BaseActivity.java
│   BasePresenter.java
│   BaseView.java
```

# References
  - [https://github.com/ribot/android-guidelines/blob/master/project_and_code_guidelines.md](https://github.com/ribot/android-guidelines/blob/master/project_and_code_guidelines.md)
  - [https://github.com/googlesamples/android-architecture/tree/todo-mvp](https://github.com/googlesamples/android-architecture/tree/todo-mvp)

## Contributor(s)
 * Amin Mastani [https://mastani.app](https://mastani.app)
