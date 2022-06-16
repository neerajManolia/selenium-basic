# selenium-basic
selenium basic
public static void main(String[] args) throws IOException {

		File f;
		FileOutputStream fos;
		HSSFWorkbook wb;
		HSSFSheet sh;
		HSSFRow rw;
		HSSFCell cl;
			
				
		f= new File("E:\\web\\Data1.xls");
		fos = new FileOutputStream(f);
		wb= new HSSFWorkbook();
		sh = wb.createSheet();
		
		for(int i=0; i<=2; i++)
		{ 
			rw = sh.createRow(i);
			for(int j=0; j<=2; j++)
			{
				cl = rw.createCell(j);
				cl.setCellValue("R"+i +"C"+j);
			}
		}
		
		wb.write(fos);
		wb.close();
		fos.close();
System.out.println("Excel Write Operation is complete!");
			
			}

}
