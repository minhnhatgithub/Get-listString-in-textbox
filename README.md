 *GET LIST STRING IN TEXT BOX*
 
 
 
 
 
 
 
 
 List<string> datta = txtlistphonenumber.Lines.ToList();
  datta = MinhNhatADB.RemoveEmptyItems(datta);
  listphone = datta.ToList();
  List<string> obj = this.listphone;
  lock (obj)
  {
      bool flag4 = this.listphone.Count == 0;
      if (flag4)
      {
          MessageBox.Show("Vui lòng điền số điện thoại cần liên lạc", "Thông Báo", MessageBoxButtons.OK, MessageBoxIcon.Information); ;
          return;
      }
      dattaphone = this.listphone[0];
      this.listphone.RemoveAt(0);
  }
