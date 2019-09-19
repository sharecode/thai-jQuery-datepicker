# thai-jQuery-datepicker
ตัวอย่างการใช้งาน ปฏิทิน ปีพ.ศ. ด้วย jQuery.datepicker ที่(มัก)ง่ายที่สุด

เป้าหมายของสคริปตัวนี้คือ ปรับช่อง Input ให้สามารถใส่วันที่ ไทยได้ รูปแบบ

วัน / เดือน / ปี พ.ศ. ไทย

ใช้ 
jquery.datetimepicker.css
jquery-2.2.4.min.js
jquery.datetimepicker.full.min.js
ตากตัวอย่างไฟล์

ไฟล์เดิม  ของ jquery datetime picker ได้เลย
เพิ่มโค้ดเข้าไปนิดนึง
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

หรือจะ โหลดไฟล์ก็ได้ เพราะใช้ซ้ำหลายรอบพิมพ์บ่อยๆจะเบื่อซะเปล่าค่ะ
<script src="./thai.datepicker.js"></script>

จากนั้นก็เรียกใช้
<script>
$(function() {thaiDatepicker("#d1,#d2,#d3")})
</script>
โดยให้ใส่ไว้ ท้ายไฟล์ หรือ หลัง element ที่จะปรับให้เป้น date timepicker

ในตัวอย่างใช้ สามตัว รวดเดียวเลยคือ 
id = 'd1'
id = 'd2'
id = 'd3'

แค่นี้แหละจบเลย
