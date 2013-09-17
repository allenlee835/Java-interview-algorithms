   //3、两个字符串的最长公共字符子串问题
	static int maxSubstring(String str1,String str2){
		String [][] str ; 
		String temp;
		int comp=0;
		if (str1.length()<=str2.length()) {
			str =new String[str1.length()][str1.length()];
			str=allsubStrs(str1);
			temp=str2;
		} else {
           str= new String[str2.length()][str2.length()];
           str=allsubStrs(str2);
           temp=str1;
		}
		for (int i = 0; i < str.length; i++) {
			for (int j = 0; j < str.length; j++) {
				if (str[i][j]!=null&&temp.contains(str[i][j])) {
					int len=0;
					len=str[i][j].length();
					if (len>comp) {
						comp=len;
					} 
				}
			}
		}
		
		return comp;
	}
	//3.1 求出一个字符串的所有可能出现的子串
	static String [][] allsubStrs(String str){
		//str="GCCCTAGCCAGDE";
		//String str2="";
		int len=str.length();
		String [][] str3 = new String[len][len];
		for (int i = 0; i < len; i++) {
			for (int j = len; j > i; j--) {
				//str2+=str.substring(i,j)+" ";
				str3[i][j-1]=str.substring(i,j);
			}
		}
		//System.out.println(str2);
/*		for (int i = 0; i < str3.length; i++) {
			for (int j = 0; j < str3.length; j++) {
				System.out.print(str3[i][j]+" ");
			}
			System.out.println(" ");
		}*/
		return str3;
	}
