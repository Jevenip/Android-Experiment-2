# 实验 2 Android界面布局

## 实验环境

- 开发环境：Android 7.0
- 软件工具：Android Studio Koala 2024

## 实验目标

1. 学习并掌握 Android 布局的基本类型：ConstraintLayout、LinearLayout 和 TableLayout。
2. 使用上述布局类型完成界面设计和实现特定功能。

## 实验步骤

### 1. 线性布局实验

- 任务：利用 LinearLayout 实现一个简单界面布局。

- 步骤：

  1. 打开 Android Studio，创建一个新的 Android 项目。
  2. 编辑 `activity_main.xml` 文件，将布局设置为 LinearLayout。
  3. 添加多个子视图（如 `TextView` 和 `Button`），排列方式设为垂直或水平。

- 关键代码：

  ```xml
  <LinearLayout
      android:layout_width="match_parent"
      android:layout_height="match_parent"
      android:orientation="vertical">
      <TextView
          android:layout_width="wrap_content"
          android:layout_height="wrap_content"
          android:text="欢迎来到线性布局实验" />
      <Button
          android:layout_width="wrap_content"
          android:layout_height="wrap_content"
          android:text="点击我" />
  </LinearLayout>
  ```

### 2. 表格布局实验

- 任务：利用 TableLayout 实现一个表格界面布局。

- 步骤：

  1. 在 `activity_main.xml` 文件中将布局类型改为 TableLayout。
  2. 定义多行多列的表格，通过 `TableRow` 添加内容。

- 关键代码：

  ```xml
  <TableLayout
      android:layout_width="match_parent"
      android:layout_height="wrap_content">
      <TableRow>
          <TextView
              android:text="姓名" />
          <TextView
              android:text="张三" />
      </TableRow>
      <TableRow>
          <TextView
              android:text="年龄" />
          <TextView
              android:text="20" />
      </TableRow>
  </TableLayout>
  ```

### 3. 约束布局实验 1

- 任务：利用 ConstraintLayout 实现更复杂的界面。

- 步骤：

  1. 将布局文件类型改为 ConstraintLayout。
  2. 设置子视图的约束条件，如顶部对齐、左对齐等。

- 关键代码：

  ```xml
  <ConstraintLayout
      android:layout_width="match_parent"
      android:layout_height="match_parent">
      <Button
          android:id="@+id/button1"
          android:layout_width="wrap_content"
          android:layout_height="wrap_content"
          app:layout_constraintTop_toTopOf="parent"
          app:layout_constraintStart_toStartOf="parent"
          android:text="按钮1" />
  </ConstraintLayout>
  ```

### 4. 约束布局实验 2

- 任务：基于 ConstraintLayout 完成更复杂的布局，涉及图片资源。

- 步骤：

  1. 下载图片资源并添加到项目的 `res/drawable` 文件夹中。
  2. 在布局文件中添加 `ImageView` 并设置约束条件。

- 关键代码：

  ```xml
  <ImageView
      android:id="@+id/imageView"
      android:layout_width="200dp"
      android:layout_height="200dp"
      android:src="@drawable/sample_image"
      app:layout_constraintTop_toTopOf="parent"
      app:layout_constraintEnd_toEndOf="parent" />
  ```

## 实验结果

通过本次实验：

1. 掌握了 Android 的三种布局：线性布局、表格布局和约束布局。
2. 成功实现了实验要求的界面设计。

## 实验心得

本次实验让我深刻理解了 Android 布局的重要性。在学习过程中，我意识到：

- 不同布局类型适用于不同的场景。
- ConstraintLayout 功能强大，但需要更详细的约束条件定义。
- 实验过程中对 Android Studio 的使用更加熟练，尤其是布局编辑器。

## 参考文献

- [Android 官方文档 - 布局](https://developer.android.google.cn/guide/topics/ui/declaring-layout.html)
- [Android 官方文档 - ConstraintLayout](https://developer.android.google.cn/training/constraint-layout)