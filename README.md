# thai-jQuery-datepicker
#ตัวอย่างการใช้งาน ปฏิทิน ปีพ.ศ. ด้วย jQuery.datepicker ที่(มัก)ง่ายที่สุด

เป้าหมายของสคริปตัวนี้คือ *ปรับช่อง Input ให้สามารถใส่วันที่ ไทย*  รูปแบบ

*วัน / เดือน / ปี พ.ศ. ไทย*

และ ปัญหาปีอธิกสุรทิน (Leap Year) ลีปเยีย ... ประมาณนี้นะ ของแท้ต้องมีวันที่ 29/02/2559 , 29/02/2016

ใช้ ไฟล์ หลักดิบๆ ไม่ได้แก้อะไรใดๆทั้งสิ้น
```
jquery.datetimepicker.css,
jquery-2.2.4.min.js,
query.datetimepicker.full.min.js 
```
จากตัวอย่างไฟล์ เพิ่มโค้ดเข้าไปนิดนึง หลัง query.datetimepicker.full.min.js  
```
function thaiDatepicker(el) {
    $.datetimepicker.setLocale('th')
    $(el).attr('readonly', true)
    $(el).addClass('date-readonly')
    $(el).datetimepicker({
        timepicker: false,
        format: 'd/m/Y',
        lang: 'th',
        yearOffset : 543,
        validateOnBlur: false,
    })
}
```

หรือจะ โหลดไฟล์ก็ได้ เพราะใช้ซ้ำหลายรอบพิมพ์บ่อยๆจะเบื่อซะเปล่าค่ะ
```<script src="./thai.datepicker.js"></script>```

จากนั้นก็เรียกใช้
```
<script>
$(function() {thaiDatepicker("#d1,#d2,#d3")})
</script>
```
โดยให้ใส่ไว้ ท้ายไฟล์ หรือ หลัง element ที่จะปรับให้เป้น date timepicker

ในตัวอย่างใช้ สามตัว รวดเดียวเลยคือ 
```
id = 'd1'
id = 'd2'
id = 'd3'
```
แค่นี้แหละจบเลย [จิ้มโหลดได้เลย](https://github.com/sharecode/thai-jQuery-datepicker/archive/master.zip).

