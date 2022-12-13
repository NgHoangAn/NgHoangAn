=============================================================
============================HTML=============================
=============================================================
=============================================================
=============================CSS=============================
=============================================================

# Selector
# bg
    background-image: url()
    background-repeat:  no-reapeat
                        repeat
                        repeat-x
                        repate-y
    background-position: position1 position2
        ko lặp và hiển thị ở vị trí nào đó
        pos1,pos2: top bot left center right
    background-attachment: value
        đứng im khi scroll
        value: fixed    // đứng im
                scroll // di chuyển theo khi kéo
    ghi tắt

# color
    hsl(hue, saturation,lightness)
    rgba
    hsla

# font

# text
    text-transform
    text-align: value
        vị trí text
        value: center left right justify
    text-decoration:

# float
    left
    right
    none
    khi dùng float thì phần nối tiếp với thẻ chứa thẻ float sẻ bị thẻ float đè lên()-> dùng overflow:hidden trong thẻ cha chừa float

# link

# border

# display
    inline
        hien thi tren cung 1 hang va chieu rong phu thuoc vao nd  ben trong thẻ
        span,a,strong,b,i,...
        ko dung được margin:top/bottom 
    block
        chiếm 1 khối
        chiều rộng = 100%

    inline-block: dạng khối nằm trên 1 hàng
    none
# margin-padding
    margin: tao k/cach giua 2 the html
    padding: tao k/cach giua the html va noi dung cua no
    box-model:
        padding-margin-border
    padding:
        dang co ban
        dạng tổng quát:
            padding với 4 g/trị
            padding với 3 g/trị
            padding với 2 g/trị
            padding với 1 g/trị
# position
    static: mặc định
    relative: định vị tuyệt đối, các thẻ html bên ngoài coi nó là cha
    absolute: định vị tương đối theo thẻ cha or thẻ body nếu ko có khai báo
    fixed: định vị tương đối cho cửa sổ Bowser của trình duyệt
    inherit: thừa hưởng các thuộc tính từ t/phần cha
    - relativev là khung - absolute là con có thể di chuyển bên trong khung đến bất kỳ vị trí nào kể cả ngoài khung.
# menu dọc
# position fixed
# z-index
    chỉ được gán cho thẻ có khai báo position:absolute
    2 thẻ có cùng z-index: thẻ nằm dưới thì hiển thị phía trên, con nằm trên cha
# clearfix
    điều chỉnh vùng ko gian của thẻ cha so với thẻ con có dùng float(dùng float thì chiều cao của thẻ cha là 0px so với thẻ con float đó - chiều cao của thẻ cha sẻ được tăng lên khi nội dung bên trong nó ko sử dụng float)
    dùng clear:both vào after
# after - before
    after: thêm nội dung vào sau thẻ html
    before: thêm nội dung vào trước thẻ html
    nội dung thẹm bằng after - before ko dùng chuột bôi đen hay copy được
# combinators
    descendant selector(space): chọn tất cả những thẻ con nằm trong 1 selector
    child selector(>): chọn tất cả những thẻ con của 1 selector nào đó
    Adjacent sibling(+): chọn tất cả những thẻ anh/chị/em rout65 nằm liền kề ngay sau 1 selector
    General sibling(~)
# list

# overflow
# Pseudo- classes
# Pseudo- elements
# unit
# Specificity
# table
# align
# Responsive
# Parallax

=============================================================
==========================JAVASCRIPT=========================
=============================================================
# variable

    + biến là nơi chứa dữ liệu

    + luôn luôn khai báo biến với const

    + dùng let nếu g/trị của biến có thể thay đổi

    + dấu = là assignment(gán) toán tử

    + dấu == là "equal to" (tương đương)

    + biến sau khi khai báo ko có g/trị là undefined

    + có thể khai báo lại 1 biến với var (ko thể với let, const)
    
    + let:
        + ko thể khai báo lại

        + phải khai báo trước khi dùng
            + dùng trước khi khai báo thì error "ReferenceError"

        + phạm vi là block ( { block } )

    + const:
        + ko thể khai báo lại

        + ko thể gán lại g/trị
            + phải gán g/trị khi khai báo lần đầu (duy nhất)

        + phải khai báo trước khi dùng
            + dùng trước khi khai báo thì error "ReferenceError"

        + phạm vi là block ( { block } )

        + dùng khi biết được g/trị của nó ko thể thay đổi
            + new Array
            + new Object 
            + ở array và object thì const ko đ/nghĩa g/trị mà đ/nghĩa tham chiếu đến g/trị
                    + ko thể gán lại g/trị
                    + ko thể gán lại array
                    + ko thể gán lại object

                    + có thể thay đổi p/tửs(element) của array
                    + có thể thay đổi thuộc tínhs(properties) của object
            + new Fn
            + new RegExp

# operator
    + toán tử số học
    + toán tử gán
    + toán tử so sánh
    + toán tử logic
    + toán tử có điều kiện
    + Loại toán tử 

# data type

    + khi add 1 số và 1 chuỗi thì js sẽ coi số này là chuỗi

    + 1 biến ko có g/trị thì là "undefined"

    + empty value không liên quan đến undefined

# END

# Function

## basic
    + có phạm vi là block

    + thực thi khi bị gọi (invokes it)

    + khi đạt được return => stop thực thi(executing)

    + khi gọi hàm mà ko có g/trị trong () => return fn object thay vì fn result

    + fn là 1 object -> nên có thể có prop và mothod

    + fn hoisting -> chỉ áp dụng fn declaration
## các loại fn
    + Fn Declarations(khai báo hàm)
        + không thực thi ngay -> "saved for later use" -> chạy khi gọi (invoked)

    + fn Expression(biểu thức hàm)
        + const ... = fn(...) {...}
        + là 1 anonymous fn ( fn no name )
        + chạy khi dùng tên biến

    + fn constructor
        + new Function (ko nên dùng)

    + anonymous fn
        + một hàm không có tên
        + tất cả đều được tạo trong thời gian chạy ứng dụng
    + arrow fn
        + ko tồn tại this
        + ko được hoisted
        + nên dùng const thay cho var (fn expression có g/trị ko đổi)    
## self-invoking
    + fn exp có thể tự gọi lại chính mình
        + thực thi auto khi theo sau là ()
    + fn declaration ko thể tự gọi
        + (fn declaration)() // trick invoke 
## fn parameters
    + parameter(tham số)
        + fn fnName(parameter1,...)
    + argument(đối số)
        + fnName(argument1,...)

    + rule
        + ko chỉ định loại dữ liệu cho para
        + ko kiểm tra kiểu trên đối số truyền vào
        + ko k/tra đối số nhận được

    + default para
        + undefined
    
    + rest(...) para
        + phần còn lại của tham số (para)
    
    + argument object
        + là 1 array các argument được dùng khi gọi hàm
    
    + invoke a fn
        + nếu fn ko thuộc về object nào -> belong default global object
            + fnName() same window.fnName()
                + this sẽ ở global object (window)     
## call
    + tái sử dụng method
        + dùng method trên các object khác nhau
        + 1 object có thể dùng method của object khác
    + chấp nhận đối số(argu)
        + riêng biệt // ("...","....")

    + person.fullName.call(person1, "TN", "VN")
        // Huy Nguyen, TN, VN
## apply
    + tái sử dụng method giống call
    + argument là 1 array
    + argu đầu ko phải object
        + strict mode
        + non strict           
## bind
    + object có thể mượn method của object khác
    + tránh mất this khi dùng callback       
## closures
    + các biến được tạo mà ko có từ khóa khai báo -> alway biến global (kể cả khi tạo bên trong fn)
    + var lifetime
        + global var tồn tại cho đến khi page bị loại bỏ (đến trang khác or đóng window)
        + local var tồn tại từ khi được invoke -> finished
## HOC
    + Bất kỳ hàm nào nhận một hàm khác làm đối số được gọi là hàm bậc cao hơn
    + Phương thức map giúp truyền một hàm để chuyển đổi từng mục trong một mảng
    + Filter nhận một tập hợp dữ liệu và bạn có thể chuyển một hàm có điều kiện trả về một tập hợp con của tập hợp
    + Reduce: nhận 2 đối số(accumulator và item)
 
# END

# Object

## basic
    + hầu hết mọi thứ trong js đều là object
        + boolean (define new )
        + number (define new )
        + string (define new )
        + Date / math / regExp / Array / Fn / Object

    + các g/trị đều là object ( trừ các g/trị n/thủy)
        + g/trị n/thủy: ko có prop(t/tính) or method(p/thức)
            + string / number / boolean / null / undefined / symbol / bigint
    + không khai báo string, number, boolean as object (new String()...)
    + so sánh 2 đối tượng luôn return false (== or ===)
    + dùng named làm index

    + dùng khi muốn element name là string(text)
    + có thể thay đổi các đối tượng -> xử lý theo tham chiếu, ko phải g/trị
## tạo Object?
        obj literals
            const obj = {...};
        new keyword
            function Obj(props){
                this.props = props;
            }
            const obj = new Obj('okL')
        Object.create()
            function newObj(props){
                this.props = props;
            }
            const obj = Object.create(newObj)
        Object.assign()
            const obj = {...};
            const copy = Object.assign({}, obj);
## props
    + prop là các g/trị được đặt tên
        + dùng delete để xóa 1 prop //delete person["age"]

        + lồng object
            const obj = {
                ...,
                name: {
                    ...
                }
            }
        +lồng array trong object
            const obj = {
                ...,
                name: [
                    ...,
                    {
                        ...,
                        name2: [...]
                    }
                ]
            }
## method
    + method là các actions thực hiện được trên object
        + display method
            + by name
            + in loop
            + .value
            + .stringify
## getter & setter
## constructor
        + add prop to cons
        + add method to cons    
## prototype
        + all object kế thừa các prop và method từ ng/mẫu(prototype)
        + thêm prop và method vào object
            + khi đã tồn tại object
            + thêm vào constructor
                + dùng prototype
                    + Person.prototype.contry = "VN"
                    + Person.prototype.name = fn() {
                        return this.Fname + this.Lname;
                    }
## set
        + tập hợp các g/trị duy nhất
        + new Set():
            + pass array    // const letters = new Set(["a","b","c"]);
                            // letters.add("a");
    
        + value():  return [object Set Iterator]

        + ko có keys
## sao chép các d/tượng trong js?
        shallow clone: giữ lại tham chiếu
        deep clone: tạo tham chiếu mới

# END

# Event
    + <element event='some JavaScript'>

# String
    + methods luôn trả về chuỗi mới, ko sữa chuỗi cũ

    + string là bất biến (immutable)

    + trính xuất phần tử
        + slice(start,end)
            + trích xuất p/tử trong chuỗi và return new string
            + lấy luôn start và end
            + nếu ko có end thì lấy hết từ start
            + nếu start là số âm thì lấy từ dưới lên

        + substring(start, end)
            + giống slice
            + khác start, end có g/trị bé hơn 0 thì sẽ là 0

        + substr(start, length)
            + giống slice
    
    + replace
        + thay thế g/trị chỉ định bằng g/trị khác
        + return new string
        + chỉ thay thế p/tử đầu tiên tìm thấy
            + replace all:  use /g
                            use replaceAll()
        + dùng /i : disable upper-case

    + toUpperCase()/toLowerCase()

    + concat()
        + nối chuỗi
    
    + trim()
        + remove khoảng trắng ở 2 phía của chuỗi
        + trimStart()
            + remove k/trắng chỉ ở phía bắt đầu
        + trimEnd()
            + remove k/trắng chỉ ở phía kết thúc

    + string padding
        + padStart
        + padEnd
    
    + trích xuất ký tự
        + charAt()
            + return index position
            + nếu ko tìm thấy -> return empty string
        + charCodeAt()
            + return unicode index position
            + between 0 - 65535 (UTF-16)
        + []
            + look like array ( not array )
            + nếu ko tìm thấy -> retun undefined
            + read only

    + convert về array
        + split()
            + dấu phân cách nếu bị bỏ qua -> return array chỉ có index [0]
            + dấu p/cách là "" -> return array là array kí tự đơn
    
    + tìm kiếm chuỗi
        + indexOf()
            + retun vị trí đầu tiên tìm thấy
            + return -1 if not found
            + tham số thứ 2 là start search
        
        +lastIndexOf()
            + return vị trí của lần xuất hiện cuối cùng
            + return -1 if not found
            + tham số thứ 2 là start search

        + search()
            + return vị trí khớp
            + không có tham số thứ 2
            + có thể powerful search values ( regular expressions )

        + match()
            + return array g/trị k/quả khớp
            + có thể áp dụng regular expressions

        + matchAll()

        + includes()
            + return true if trong string có chứa
            + phân biệt hoa, thường
        
        + startsWith()
            + return true if string bắt đầu với string chi định
        
        + endsWith()
            + return true if string kết thúc với string chỉ định

    split(): cắt chuỗi cho vào array theo d/kiện trong ()
        reverse(): là split xong rồi đảo ngược thứ tự trong array
        join():nối các element trong array lại với nhau theo d/kiện
        - word counter
        - slice(indexStart, indexEnd): cắt chuỗi
        - Representation of NUmber


# Template Literals
    + use back-ticks(``) đ/nghĩa string
        + có thể dùng '' và ""
        + ${...}

# Number

# Array
    + khai báo: new Array() or []
    + có thể có các biến có type khác nhau trong cùng 1 array
        + object, fn, array in array
    + dùng number làm indexes
    + dùng khi muốn element name là numbe
    + check array : isArray()
    + length
    + toString()
    + join
    + push/unshift
    + pop/shift
    + concat
    + splice(pos1,pos2, value)
        + pos1: where be added
        + pos2: how many element remove
        + value: các g/trị thêm vào
    + slice
        + cắt 1 phần của array -> new array
        + ko ảnh hưởng array cũ
    
    + sort() to anphabet
        + ko chính xác khi sort number ["25" > ""100" cuz "2" > "1"]
            + fix:
                // array up
                array.sort(fn(a, b){
                    return a- b
                })
                // array down
                array.sort(fn(a, b){
                    return b - a
                })
            + hàm so sánh
                + xác định thứ tự sắp xếp
                + return âm, 0, dương
                    + âm: a trước b
                    + dương: b trước a
                    + 0: ko thay đổi

    + reverse() đảo chiều

    + forEach()
    + map()
        + tạo ra mảng mới / ko thay đổi mảng cũ
        + ko thực thi với mảng ko có g/trị

    + filter()
        + tạo mảng mới với các element pass test

    + reduce()
        + chạy qua các p/tử trên mảng để tạo ra g/trị duy nhất
        + ko ảnh hưởng mảng cũ
        + có 4 đối số

    + every()
    + some()
    + indexOf()
    + lastIndexOf()
    + find()
    + findIndex()
    + from()
    + keys()
    + entries()
    + includes()


    array-like-object
            - kế thừa từ object
            - ko có các method của array: forEach,push,map,filter,slice
            - convert to Array
                - .from() // Array.from(arrayLike)
                - for..of //
                - spread operator // [...arrayLike]
                - Object.values // arr = Object.values(arrayLike)
                - Object.keys
            - có thể dùng call() để gọi array method đồi với array-like-object
        reduce: 
        map:
        filter
        sort: sắp xếp trên mãng đã cho
            default là theo unicode point
            custom:
                anphabet,length,number sort,even-odd
        every
        some
        có thể destructuring
        remove duplicate element
            dùng filter
            dùng Set
        spread/rest
        find
        split
        shift/pop/splice
        join
        ...

# Dates
    + new Date() : tạo ra object với ngày, giờ hiện tại

    + new Date(date string) : tạo ra objecrt từ chuỗi date

    + new Date(year, month, ...) : tạo ra object date được chỉ định
        + nếu month lớn hơn 11 -> year + 1
        + nếu day lớn hơn max -> month + 1

    + new Date(miliseconds): 

    + date method:

    + displaying dates
        + tự động chuyển object về dạng string .toString()

        + toDateString(): show in html -> Sat Dec 10 2022

        + toUTCString(): show in html -> Sat, 10 Dec 2022 13:37:44 GMT
        + toISOString(): show in html -> 2022-12-10T13:38:48.470Z

    + Date Formats
        + Date input:
            ISO:    "2015-03-25" (The International Standard)
            Short:  "03/25/2015"
            Long:   "Mar 25 2015" or "25 Mar 2015"

        + Date Output:
            Default:    Sat Dec 10 2022 20:39:06 GMT+0700 (Indochina Time)
        
        + ISO date:
            + YYYY-MM-DD
            + YYYY-MM
            + YYYY
            + YYYY-MM-DDTHH:MM:SSZ  // 2015-03-25T12:00:00Z
                                    // Date T time
                                    // Z -> UTC time (same GMT time)
                                    // remove Z change time
                                        // 2015-03-25T12:00:00-06:30
        
        + Short Date:
            + MM/DD/YYYY
                + YYYY/MM/DD is undefined
                    // some browsers return NaN
                + DD/MM/YYYY is undefined
                    // some browsers return NaN

        + Long Date:
            + MMM DD YYYY
                // Mar 25 2015
                // January 25 2015
                // JANUARY, 25, 2015
                
        + Parsing dates:
            + parse(): chuyển về miliseconds
                + let msec = Date.parse("March 21, 2012")
                    // 1332262800000
    
    + Date method:
        + new Date()
        + date get method:
            + getFullYear()
            + getMonth()
            + ...
            + getMilliseconds()
            + getTime()
            + now()
            + getTimezoneOffset() -> return chênh lệnh giữa local và UTC time
        
        + set Date method
            + same get date method
            
# math
    + ko có constructor
    + properties
        + .E        // Euler
        + .PI       // PI
        + .SQRT2    // căn bận 2 của 2
        + .SQRT1_2  // căn bậc 2 của 1//2
        + .LN2      // logarit của 2
        + .LN10     // logarit của 10
        + .LOG2E    // logarit 2 của E
        + .LOG10E   // logarit 10 của E
    
    + method
        + round(x)  // return gần x
                    // round(4.5) -> 5

        + ceil(x)   // return up lên 1
                    // ceil(4.2) -> 5

        + float(x)  // return down xuống 1
                    // float(4.9) -> 4

        + trunc(x)  //  return về p/nguyên

        + sign(x)   // return 1(+), 0(0), -1(-)

        + pow(x,y)  // return x mũ y

        + abs(x)    // return trị tuyệt đối của x

        + sin, cos, min, max

        + random(): return số <1

# booleans
    + yes / no
    + on / off
    + true / false (js)
    + Boolean()
    + as object
    
# Loop
    + for/of (object)
    + for/in (array)

# set
    + tập hợp các g/trị duy nhất
    + new Set():
        + pass array    // const letters = new Set(["a","b","c"]);
                        // letters.add("a");
    
    + value():  return [object Set Iterator]
    +

# map
    + key - value
    + set() có thể dùng để thay đổi g/trị dã tồn tại trong Map

# typeof
    + 5 loại dữ liệu chứa g/trị
        + string/number/boolean/object/fn
    
    + 6 loại đối tượng
        + object/date/array/string/number/boolean
    
    + 2 loại ko chứa g/trị
        + null/undefined

    + constructor property return constructor fn

    + biến ko có g/trị -> undefined -> undefined type

    + null -> object type

# convert
    + string to number
        + NUmber()
        + parseFloat()
            + string return -> float number 
        + parseInt
            + string return -> integer
        + đặt dấu + trước string -> number
    
    + number to string
        + toString()
        
    + Date to number
        + number()
        + getTime()
    + date to string
        + String()
        + toString()

# regExp
    + /pattern/modifiers;

# scope
    + block
    + fn
    + global

# hoisting
    + có thể dùng trước khi khai báo

    + let/const được hoisted lên top block, nhưng ko được khởi tạo
        + không sử dụng được cho đến khi khai báo
        + let -> return "ReferenceError" khi dùng trước khai báo
        + biến sẽ nằm ở "TEMPORAL DEAD ZONE" từ khi start -> được khai báo
        + const -> return "syntax error"
    
    + chỉ hoisted với biến khia báo, biến khởi tạo ko được hoisted


    - di chuyển mọi khai báo lên đầu mọi phạm vi
    - co thể sử dụng 1 iến trươc khi nó được khai báo
    - var được lưu trữ, let-const thì không
    - khởi tạo (initializations) không được hoisting,
    cac decleration là theo cơ chế

    di chuyển tất cả cac biến và hàm khi khai báo lên đầu scope trước khi thực thi
        fn declarations(bắt đầu là fn operator sau đo gán cho 1 cái tên) co hoisting
        fn expression(tạo 1 variable sau gán với 1 anonymous fn) thì ko

# use Strict
    + ko thể dùng các biến khi chưa được khai báo

# this
    + dùng trong object
    + trong cùng object -> refers object
    + khi 1 mình -> refers global object
    + trong fn -> refers global object
    + torng fn (strict mode) -> refers undefined
    + trong event -> refers element nhận event đó
    + call, apply, bind -> refers object bât kì

    bind(): gọi hàm với ngữ cảnh nhât định
            không gọi hàm, chỉ sữa ngữ cảnh
    call() và apply(): gọi hàm ngay lập tức và sửa đổi ngữ cảnh
        call(): accept 1 danh sách các g/trị làm đối số
        apply(): accept 1 mảng làm đối số
    dùng bind khi sửa ngữ cảnh và gọi hàm sau này
    dủng call và apply khi sữa ngữ cảnh và gọi hàm ngay lập tức

# arrow fn
    + this luôn đại diện cho object xác định c/năng arrow fn

# class
    + constructor
        + luôn phải có tên "constructor"
        + auto chạy khi có object mới được tạo
        + dùng để khởi tạo thuộc tính cho object
        + nếu ko đ/nghĩa 1 mothod constructor thì JS sẽ tự động tạo empty constructor mothod
    
    + class ClassName {
        constructor() {...}
    }
    + k phải là object
    + là template(khuôn mẫu) cho object
        + khi có class -> có thể tạo object từ nó
    + luôn luôn phải có constructor method
    + dùng extends để kế thừa 1 class
        + super() đề cập đến class cha
            + phải gọi super mới dùng được các prop và mothod của class cha
    + getter va setter
        + có thể dùng trong class
        + dùng khi muốn làm gì đó với prop trước khi return
    + class declartion ko được hoisted
    + static mothod
        + đ/nghĩa trong chính class đó
        + class ...(){
            ...
            static ...(){...}
        }
        + ko thể gọi trên 1 object mà phải trên object class
            myCar = new Car("BMW")

                Car.hello()     //work
                myCar.hello()   // NOT work

# module
    + chia file
    + import/export
        + export default
            + trên 1 file chỉ có 1 default
            + export deafult ...;
        + export { ..., ... }

# JSON
    + name - value
    + cách nhau = ","
    + {} cho object
    + [] cho array
    + chuyển JSON về object
        + JSON.parse(text_json_var)
        + text_json_var là 1 string
    
    + JS object Notation
    + định đạng text để lưu trữ và tao đổi data
    + why?
        + format text only -> easy sent <-> computer
    + JSON.parse -> convert JSON string to js object
    + JSON.stringify -> convert object to JSON string
    + syntax rules
        + name/value
            "name":"Huy"
        + phân tách = ,
        + { } cho object
        + [ ] cho array

    + json value
        + string / number / object / array / boolean / null 
            (trừ fn / date / undefined )
    + JSON vs XML
    ...

# stylel guide

# async
    + callback
        + fn được truyền dưới dạng argument(đ/số) cho fn #
        + fn có thể gọi fn khác
        + callback fn có thê chạy sau khi fn # kết thúc
        + 
            function fn1(...){...}
            function fn2(...,callback){
                ...
                callback(...)
            }
            //
            fn2( ..., fn1 )
                // fn1 là 1 callback
                // fn1 được truyền nhứ 1 argument cho fn2


                Callback function
    - một hàm được thực thi sau khi một hàm khác đã thực thi xong
    - một hàm được truyền cho một hàm khác như một đối số và được thực thi sau khi một số tác vụ đã hoàn thành
    cho 1 hàm là tham sô của hàm khác, tham số(fn) được lưu lại và sẻ thực thi khi co kết quả(dữ liệu tả về or lỗi khi thao tác)
            callback hell là callback lồng trong callback
    
    + Async
        + fn chạy song song với fn khác
        + setTimeout
        + setInerval
    
    + Promise
        + prop( state, result )
            + pending
                result -> undefined
            + fulfilled
                result -> value
            + rejected
                result -> error object

        + khởi tạo new Promise với fn với 2 tham số resolve và reject
            + đặt code bât đồng bộ trong fn Promise
                + resolve khi mọi thứ xảy ra như mong muốn
                + reject khi không
                + 
                    let myPromise = new Promise(res, rej){...}

                    myPromise.then(
                        fn(value){...}
                        fn(error){...}
                    )
                
            + mỗi .then nên trả về 1 promise

            + chỉ có 1 .catch để xử lý toàn bộ error(khi có lỗi thì promise chain ngừng và nhảy vào .catch)

            + không thể truy xuất biên được truyền or khai báo trong promise chain ngoài phạm vi promise

            + phải co ít nhất 1 .catch ở cuối promise để băt lỗi(nếu ko thì bất kỳ lỗi nào xảy ra đều sẻ bị bỏ qua)



            trạng thái
        Pending: chờ xử lý
        fulfilled: hoàn thành
        rejected: từ chối
    ưu:
        có thể kêt hợp
        có thể dễ dàng thực thi mã với Promise.all khi nhiều phản hồi được trả về
        có thể đợi một kết quả từ các lời hứa đồng thời đang chờ xử lý với sự trợ giúp của Promise.race
        có thể viết mã không đồng bộ một cách đồng bộ nếu bạn sử dụng nó kết hợp với async / await
    nhược điểm
        chỉ có thể hoạt động trên một giá trị duy nhất tại một thời điểm
        không có sẵn trong trình duyệt cũ hơn, chúng phải được làm đầy
        chậm hơn so với việc sử dụng lệnh gọi lại, điều này có thể dẫn đến các vấn đề về hiệu suất có thể xảy ra

    + async/await
        + async làm cho fn return Promise
            + đặt async trước fn (fn phải trả về 1 promise)
            + 
                async fn myFn(...){ return ... }

                same: fn myFn(...){ return Promise.resolve(...)}
                /////////////
                myFn.then(
                        fn(value){...}
                        fn(error){...}
                )

            
        + await làm cho fn đợi Promise
            + chỉ được dùng bên trong async
            + tạm dừng fn thực thi, đợi 1 promise resolved trước khi tiếp tục
            + 
                ... = await promise


async,await
        async: thông báo fn sẽ xử lý bất đồng bộ
        await: báo chúng ta muốn đợi kq của thao tác bất đồng bộ trong 1 fn có đánh dấu async.
# DOM
    + truy xuất và thao tác trên tài liệu có dạng html or xml
        + cấu trúc
            + document node: thẻ <html>
            + element node: 1 p/tử html
            + text node: bên trong 1 thẻ html dều là node text
            + attribute node: href
        + quan hệ
            + document node luôn là node đầu
            + tât cả các node đều có 1 node cha(trừ document node)
            + 1 node có thể có 1 hoặc nhiều con
            + node có cùng cha là node siblings
            + node đầu firstChild - node cuối lastChild

    + HTML DOM method
        + actions thực hiện trên HTML elements
        + Trong DOM, html element là object
        + getElementById
        + innerHTML
            + dùng để lấy nội dung của element
    
    + DOM Document Object
        + đại diện cho web page

        + find HTML element (document.)
            + getElementById(id)
            + getElementsByTagName(name)
            + getElementsByClassName(name)
            + querySelectorAll()
                + match (id, class, names, types, attribute, value, ...)

        + change HTML element (element.)
            + innerHTML = new html content
            + attribute = new value
            + style.property = new style
            + setAttribute(attribute, value)

        + add & delete Element (document.)
            + createElement(element)
            + removeChild(element)
            + appendChild(element)
            + replaceChild(new, old)
            + write(text)

        + add event handle
            + getElementById(id).onclick = function(){...}

        + find HTML Object
 
    + Form
    + DOM EventListener
        + element.addEventListener(event, function, useCapture)
            element.addEventListener("click", myFunction);
            /////////////////
            function myFunction() {
                alert ("Hello World!");
            }
        + Event Bubbling or Event Capturing
        + removeEventListener()

    + DOM Navigation
    




            document 
            element: truy xuất thông qua class, id, nanme
            event: gán onclick(), onload() vào cac thẻ html
            listener: lắng nghe sự kiện tác động lên thẻ html
            Navigation:
            node, nodelist

                innerHTML: return về mã HTML bên trong p/tử hiện tại(bao gồm element node và text node)
                outerHTML: return về tagName + innerHTML

                appendChild: thêm node con vào node hiện tại

# BOM
    + bowser object model
    + global var là prop của window object
    + global fn là method của window object
    + window size
        + innerHeight
        + innerWidth
        + .open() / .close() / .moveTo() / .resizeTo()
    + window Screen
        + ko cần prefix window
        + screen.width: return width màn hỉnh
        + screen.height: return height màn hình
        + screen.availWidth
        + screen.availHeight
        + screen.colorDepth -> return số bit dùng show 1 color
    
    + window.location
        + href      -> return URL current page
        + hostname  -> return name website
        + pathname  -> return pathname
        + protocal  -> return protocol
        + assign    -> load new DOcs

    + history
        + .back     -> trở lại trang trước
        + .forward  -> tiến tới URL tiếp theo

    + window.navigator
        + ko cần prefix window
        + .cookieEnable
            + return true if cookie enable, <=>
        + .appName
            + return app name (ko sử dụng)
        + .appCodeName
            + (ko dùng)
        + .appVersion
        + .userAgent
        + .platform
        + .language
        + .onLine
        + .javaEnabled
    
    + Popup Box
        + alert
        + confirm
        + prompt

    + timing event
        + setTimeout(fn, miliseconds)
            + chạy fn sau miliseconds
            + dừng việc thực thi -> clearTimeout(...)

        + setInterval(fn, miliseconds)
            + chạy fn sau mỗi miliseconds
            + dừng việc thực thi -> clearInterval(...)

        
        + cả 2 đều là window object
            + ko cần prefix window
    
    + cookie
        + lưu trữ data nhỏ
        + 


        gửi lên server
            (truyền từ server tới browser, được lưu trên máy khi truy cập vào ứng dụng)
            dùng chủ yếu đọc phía máy chủ
            có thời gian sống (custom)
            4KB và vài chục cookie cho 1 domain
            cach tạo:
                document.cookie = 'username=Ted Mosby; expires=Thu, 18 Dec 2018 8:00:00 UTC';
                document.cookie = 'username=Ted Mosby; max-age=9000'; //giây

cho phép JavaScript “nói chuyện với” trình duyệt. Nó bao gồm các đối tượng điều hướng, lịch sử, màn hình, vị trí và tài liệu là con của cửa sổ. Browser Object Model không được chuẩn hóa và có thể thay đổi dựa trên các trình duyệt khác nhau

# API
    + validation API
        + checkValidity()

        + setCustomValidity()
    + history API
        + back() : return trang url trước

        + go()   : đi dến trang được chi dịnh trong ()

        + forward() : go next url

        + length: number of urls

    + storage API
        + localStorage
            lưu trữ vô thời hạn: (xóa bằng: js, bộ nhớ trình duyệt, localStorage API)
            5MB
            không gửi thông tin lên server
            sử dụng:
                khởi tạo
                    localStorage.setItem('key','value')
                    localStorage.key = value
                    localStorage['key'] = 'value'
                lấy:
                    localStorage.getItem('key')
                    localStorage.key
                xóa:
                    localStorage.removeItem(key);
                    localStorage.clear()
        
        + sessionStorage
            lưu trên Client: giông localStorage
            mất khi đống tab
            ko gửi lên server
            <5MB

        lưu trữ cặp khóa-giá trị
    local storage: lưu trữ dữ liệu cho client mà không có ngày hết hạn
    session storage: chỉ lưu trữ dữ liệu cho một phiên. Dữ liệu sẽ biến mất khi trình duyệt bị đóng
        
        + Fetch API
            + cho phép browser thực hiện các yêu cầu http -> servers
            +
                fetch(file)
                    .then()
                ////
                async fn ...(file){
                    ... = await fetch(file)
                    ...
                }

        + Geolocation API

# AJAX
    + tác dụng
        + đọc data từ server sau khi đã load page
        + cập nhật lại trang ko cần load lại
        + gửi data lên server ở background
    + là gì?
        + sự kết hợp của XMLHttpRequest và HTML DOM
    + how??
        + có event kích hoạt
         -> tạo ra 1 XMLHttpRequest by js
         -> send request đến server
         -> server xử lý request
         -> send response về web page
         -> response được đọc bởi js
         -> thực hiện actions
    
    + XMLHttpRequest
        + xAjax = new XMLHttpRequest()
            xAjax.onload = fn(){

            }
            xAjax.open(mathod,url,async,user,psw)
            xAjax.send()
            /////////////////////////
        + method
            + abort()       -> chủy request hiện tại
            + getAllResponseHeaders -> return header info
            + getResponseHeader     -> return header info cụ thể
            + open(
                method,                 // GET(most use) or POST
                url,                    // file location
                async,                  // true(async)(default) or false  
                                            (sync)
                user,                   // user name (optional)
                psw)                    // password (optional)
                                    -> chỉ định request
            + send()                -> send request to server (GET)
            + send(string)          -> send request to server (POST)
            + setRequestHeader()    -> add label/value vào header sẽ send
        
        + prop
            + onload                -> x/định fn sẽ gọi khi nhận request
            + onreadystatechange    -> x/định 1 fn sẽ được gọi 
                                        khi prop readState thay đổi
            + readState             -> giữ trạng thái của XMLHttpRequest
                                        // request not init
                                        // server connection
                                        // được request
                                        // xử lý requqest
                                          kết thúc request và response ready
            + responseText          -> return response as string
            + responseXML           -> return response as XML data
            + status                -> status-number
                                        // 200: "OK"
                                        // 403: "Forbidden"
                                        // 404: "Not Found"
            + statusText            -> return status text


    cách hoạt động:
        sự kiện xảy ra-->request lên server-->reponse về web-->xử lý bằng js
    ưu:
        cập nhật trang mà ko tải lại trang
        yêu cầu và nhận dữ liệu từ máy chủ sau khi tải xong
        gửi dữ liệu đến máy chủ ở background
    nhược:
        không hoạt động khi Js bị disabled

# jquery
# graphics

# ES5
    + "use strict"
    + charAt()
        + return character at a index
    + string trên nhiều dòng
        + dùng "\" hay "+"
    + trim()
        + xóa k/trắng 2 bên string
    + isArray()
    + reduce
    + reduceRight
    + stringify
        + chuyển về dạng json
    + bind()
        + 
# ES6
    + (spread)... operator và (rest)... operator
        + phần còn lại 
# ECMAScript 16
    + **
    + **=
    + includes()
# ECMAScript 17
# ECMAScript 19
# ECMAScript 20
# ECMAScript 21


=============================================================
==========================REACT==============================
=============================================================
# ES6
    -variable
        var:
            scope là global(trừ khi khai bao trong fn thì là fn scope)
            có tinh hoisting: biến sẻ được đưa lên đầu scope trươc khi thực hiện( giá trị là undefined)
        let:
            scoppe là block
            cho phep cập nhật giá trị của biến, ko cho tái khai báo lại biến
            có tinh hoisting: (gia trị là Reference Error)
        const:
            scope là block
            có hoisting (gia trị là Reference Error)
            đôi với kiểu là primitive(string, number, boolean,null,undefined) thì ko thể tái tạo biến hay cập nhật
            đôi vơi kiểu là reference(object, array, fn) co thể cập nhật giá trị
    - default parameter
    - Spread  
        lặp lại các p/tử của mãng or object
    -  rest
    - destructuring
    - arrow fn
    - classes
    - import & export

# virtual DOM
    - xây dựng dựa trên DOM thật
    - khi render 1 jsx element ->cập nhật virtual DOM(kiểm tra sựu thay đổi với virtual DOM trươc đó =>cập nhật)-> cập nhật DOM thật
    - tại sao dùng?
        - khi 1 nodes thay đổi thì cac nodes cũng thay đổi trên DOM thật -> chậm khi xây dựng ứng dụng lớn.

# jsx
        là js XML: cho phép viết mã html trong React
        gán 1 biểu thức trong jsx = cách bọc nó trong {}
        là 1 biểu thức:
            sau khi complie => các đoạn mã jsx sẽ như các object thông thường
        phần tử con trong jsx
            nếu chỉ co 1 tag thì đóng = />
            co nhiều ptu73 con => bọc bằng jsx tag(<div></div>)
![](html convert jsx.png)

# components
        - bên trong return luôn tồn tại tag bao ngoài tất cả
        - dùng React.DOM để render 1 component
        - phải có cấu trúc XML <Ten> or <Ten></Ten>
        - chia nhỏ các thành phần trong UI thành nhiều component
        - class component
            cách viết:
                class ... extends Component {
                    render(){
                        return(
                            ...
                        )
                    }
                }
                export default ...;
            thoải mái dùng state, props, lifecycles
        - fn component
            cách viết:
                const ... = fn(props){
                    return(
                        ....
                    )
                }
                export default ...;
            ko có khái niệm state, life cycles, events (khi dùng Hooks mới có)

# props, *state
    - props là tham số
    - là 1 object
    - component nhận vào 1 props và trả về 1 react element
    - khi 1 component cha truyền cho component con 1 props -> component con chỉ có thể đọc và ko có uyền chỉnh sửa no bên phía component cha
    - truyền props:
        - truyền 1 g/trị bên trong 1 tags thì nó có thuộc tính chirlden trong object props
        - vi dụ :
            const app = () => <Welcome name="Huy" age=18>hello</Welcome>
    - bên trong component : giá trị là 1 object
        {
            name: "Huy",
            age: 18,
            children:"hello"
        }
    - nhận props:
        class component: dùng this.props
        fn component: chỉ định tham số trong fn
    - props validation
        kiểm soát vấn đề của props, kiểm tra đầu vào của props trước khi component được render.
        dùng propTypes
            fn component
                fnComponent.propTypes = {
                    ....//
                }
            class component
                clComponent.propTypes = {
                    ...//
                }
            or dùng:
                static propTypes = {
                    ...//
                }
    - xử lý data truyền vào cho 1 component
    - xử lý data giữa các component
    - xử lý data khi các component lồng vào nhau
    - xử lý đk khi render(login/logout)
    - xử lý array/object -> html list
    =====================================
    - state là 1 object lưu trữ giá trị của các thuộc tính bên trong component, scope là component đó, giá trị của 1 state thay đổi-> component render lại.
            khởi tạo:
                dùng this.state = {name:"Huy"};
            lấy g/trị
                gọi this.state
                    this.state.name// log "Huy"
            nên khởi tạo state trong hàm contructor(hàm chạy đầu tiên khi component được gọi)
            cập nhật state
                dùng this.setState({
                    name: "HuyRua"
                })

    component API
        setState()
            cập nhật g/trị của state, tham số truyền vào của API là giá trị của state muốn update
                this.setState({
                    ....//
                })
            or là 1 fn callback gồm tham số: state trước, props có trong component
                this.setState((prevState, props) =>{
                    return newState;
                })
        forceUpdate()
            re-render mà ko cần bất cứ sự thay đổi nào của state
            this.forceUpdate
        findDOMNode()
        bind()

# lifecycle
        khi render 1 component thì react thực hiện nhiều tiến trình # nhau
        các giai đoạn
            Initialization
                khởi tạo state và props(thường trong constructor)

            Mounting

                - thực hiện sau khi khởi tạo hoàn thành
                - nv: chuyển virtual DOM thành DOM và hiển thị
                - component render đầu tiên
                - có 2 p/thức:

                    componentWillMount():
                        chạy khi component chuẩn bị được mount(trước khi render)-> component được mount
                        không nên thực hiện bất cứ thay đổi nào liên quan đến state, props hay call API ở trong hàm này
                            vì thời gian chuẩn bị mount -> mount rất ngắn nên các tác vụ đó không thể hoàn thành kịp

                    componentDidMount():
                        gọi sau khi đã mount, xảy ra sau khi componentWillMount thực hiện xong.
                        có thể gọi API, thay đổi state, props

            Updating

                giai đoạn 3
                data của props & state sẽ được update -> đáp ứng event của user -> re-render component
                các p/thức:

                    shouldComponentUpdate:
                        xác định component có nên được render (default-> return true)
                        nhận vào 2 tham số : nextState, nextProps

                    componentWillUpdate:
                        gọi trước khi tiến hành re-render
                        action: update state, props trước khi re-render
                        nhận vào 2 tham số : nextState, nextProps

                    componentDidUpdate:
                        gọi khi component đã re-render xong

            unmounting

                bước cuối
                tiến hành unmountDOM

                    componentWillUnmount:

# handling events
        các event viết trong {}
        dùng preventDefault(): chặn các hành động mặc định

# xử lý form
    tạo state chứa giá trị của input trong hàm constructor
    bắt sự kiện onchange
    vd form
# render với điều kiện
    gan element vào biến
    biểu thức điều kiện torng jsx
    ngăn chặn component render
# List and Key
    lists: 
        khởi tạo giống js
        const list = ['a','b','c'];
    keys:
        là duy nhất khi ss với anh/chị của nó trong lists chứa chúng
        tránh lấy index làm key(sắp xếp mảng thì index thay đổi-> xác định lại key 1 lần nữa-> giảm hiệu xuất làm việc)
            dùng index làm key khi
                là list tĩnh, ko thay đổi
                ko sắp xếp lại
                ko được lọc
                ko có id cho mục trong list
# Lifting State Up
    khi 1 component thay đổi(re-render) thì các component quan hệ phía trên nó phải nhận được sự thay đổi(cha/con)
# Refs
    tham chiếu 1 element trong DOM or từ con -> cha(đọc- chỉnh sửa element)
    vd....
        refs(cây cầu) khi 1 element gán vào 1 refs -> cho phép sửa đổi, truy cập vào element đó ngay lập tức (ko cần dùng đến props hay state để component re-render)
    cách dùng:
        khởi tạo: thường trong constructor(class component) hay biến(fn component) -> gán vào 1 element trong hàm render()
            ....
            constructor(props){
                ...
                this.myRefs = React.createRef();
            }
            render(){
                return(
                    ....
                    ref = {this.myRefs}
                )
            }
            //khởi tạo 1 ref(dùng React.createRef()) -> gán g/trị vào thuôc tính myRef trong class/fn component -> gán refs vào element input(element có thể được truy cập/sửa thông qua ref)
        uses:
            ...
            handleClick = () => {
                ...
                this.myRef.current.focus();
                ....
            }
            //curent: chứa g/trị element được tham chiếu khi element đó được render -> focus vào input(ko dùng đến state or props->ko re-render)
    Forwarding Refs:
        chuyển 1 ref từ 1 component tới component con, cho phép component cha tham chiếu tới các element của component con để đọc/chỉnh sửa
        - cách dùng:
            bao component con trong React.forwardRef()
# Context
    chia sẻ dữ liệu tới các component trong cây mà ko cần truyền dữ liệu qua props theo từng cấp bậc
    khởi tạo:
        const MyContext = React.createContext(defaultValue)
            //defaultValue = g/trị của props value trong provider
            //context object
        mỗi context object phải đi kèm 1 provider(nhận về sự thay đổi của context)
        <MyContext.Provider value={}>
        <MyContext.Consumer>
            //khởi chạy khi giá trị context thay đổi -> nhận về g/trị của context đó
        .displayName
            // hiển thị trong devTools
        .contextType: được tạo bởi .createContext -> lấy g/trị của context
    cách dùng:
        - khởi tạo(.createContext) -> nhận 1 object các thuộc tính: provider, consumer
        - dùng provider bọc quanh component, truyền g/trị vào props value
        - thêm consumer ở bên trong provider để chia sẻ context(lấy g/trị thông qua props.chirlden)
        vd
# Fragments
    bao bọc các element jsx -> triển khai element theo mong muốn
    cach viết:
        React.Fragment key={}//chỉ định key vào fragment(triển khai lists..)
        <></>
# Render props
    - tái sử dụng code
    - thực hiện -> truyền vào component 1 props có value như là 1 fn
    - vấn đề:   
# higher other component
    là 1 fn nhận vào 1 component và trả về 1 component
# redux

# Hook
    cho phép sử dụng state, life cycle trong fn component
    - useState():làm việc với state trong fn component mà ko chuyển về class component
        const [tenState. hamCapnhatState] = useState(giaTriBanDauCuaState)
        cach dùng:
            import vào useState from 'react'
        - co thể lưu bất kì kiểu dữ kiệu nào trong state: object,number,string,...(ko giống như class component chỉ lưu trong object)

    DOM events/ custom event
    (why remote event listener)
    Observer pattern: subcribe / unsubcribe
    closure

    useEffect(): chạy khi g/trị của 1 biến nào đó thay đổi or component được render (thay thế life cucle trong class component)
        useEffect(fnDuocKhoiChay, arrChuaCacGiaTriThayDoi)
        - là componentDidMount, componentDidUpdate, componentWillUnmount kết hợp lại
        - sử dụng useEffect như componentDidMount
            - useEffect(effectFn, [])
            - dùng để gọi API khi component được render
        - sử dụng useEffect như componentDidUpdate
            - useEffect(effectFn)
        - sử dụng useEffect như componentUnWillMount
            - chỉ cần return về 1 fn trong effectFn, fn được return đóng vai trò như componentUnWillMount


    - useContext(): nhận về g/trị của context mỗi khi nó thay đổi
        const gtriContext = useContext(tenContext);

    - useReducer(): xử lý chia sẻ state giữa các component
        const [state, dispatch] = useReducer(reducer, initArg, init)
    - Custom Hook
    - useRef 
# Router
    react-router-dom
 
=============================================================
==========================THUẬT TOÁN=========================
=============================================================

# Linear Search
    - tìm kiếm p/tử cho trước trong 1 danh sách = duyệt lần lượt từng p/tử của danh sách -> tìm được or hết
    - cách:
        băt đầu duyệt từ đầu đến cuối mảng với x
        p/tử  đang duyệt = x thì return vị trí
        ko tìm thấy or hết -> return -1
        độ phức tạp là O(1) -> O(n) 
# Binary Search
    - tìm kiếm vị trí trongn mảng đã sắp xếp
    - chia khoảng tìm kiếm thành 1/2 -> ss x với giá trị ở giữa
        - nếu g/trị nhỏ hơn g/trị ở giữa thì tìm bên trái, ngược lại
         
# Interpolation Search
    - có xu hướng tiến đến gần vị trí, giá trị tìm kiếm.
    - tìm ra phần tử gần với giá trị tìm kiếm  nhất và bắt đầu từ đó để tìm
    - cách tìm:
        - x là số cần tìm, t là tập
        - s = left +(right-left) * 1/2
        - thay 1/2 = (x - t[left]) / (t[right] - t[left])
        - ta được:
            s = left + (x - t[left]) * (right - left) / (t[right] - t[left])
        - nếu t[s] === x thì return, ko thì có 2 trường hợp:
            - t[s] < x ==> left = s + 1
            - t[s] > x ==> right = s - 1
# Bubble Sort
# Insertion Sort
# Selection Sort
# Merge Sort
# Quick Sort

============================TODAY============================
selector
    + tìm kiếm html element
    + 
        name, id, class
        combinator
        pseudo-class
        pseudo-element
        attribute
    + #id / .class / element.class / * / element / element, element...
add css
    + external
    + internal
    + inline
colors
    + RGB / Hex / HSL / RGBA / HSLA
    + RGB(red, green, blue) // [0-255]
    + RGBA(red, green, blue, alpha) // anpha [0.0 - 1]
    + HEX(#rrggbb) or (#rgb)  // [0-255]
    + HLS(hue, saturation, lightness)
        + hue [0-260] rgb/3
        + saturation 0-100%
        + lightness 0-100%
    + HLSA
        + anpha [0.0 - 1]

background
    + -color
    + -image: url("")
    + -repeat 
    + -attachement
        + có 2 g/trị: scroll or fixed
    + -position
    + -clip / origin / size
border
    + style
    + width
    + color
    + border: width style color
    + radius
margin
    + tạo k/trắng xung quanh element
    + value:
        + auto:
        + length
        + %: dựa vào % chiều dài của p/tử chứa
        + inherit: kế thừa margin của cha
padding
    + tạo k/trắng bện trong element
    + dùng box-sizing: border-box để giữ nguyên width element (ko phụ thuộc vào pading, border, margin)

height/width
    + max-width: chiều aco tối đa của element
box model
    + bao gồm margin / padding / border / content
outline
    + line drawn bên ngoài border
    + width
    + color
    + offset

text
front
icons
link
list
display
max-width
position
z-index
overflow
float
inline-block
align
combinators
pseudo-class
pseudo-element
opacity
navigation bar
dropdown
image gallery
image sprites
attr selector
form
counter
layout
unit
specificity
!important
math fn
rounded corners
border img
background
color
color key
grandients
shadow
text effect
web font
2d trans
3d trans
transition
animation
tooltips
style img
img reflection
object-fit
object-potion
masking
button
pagination
multiple columns
user interface
variable
box sizing
media queri
flexbox
responsive
grid
sass

=============================================================
==========================NODEJS=============================
=============================================================
# http protocol*
# SSR & CSR
    - server side rendering
        mã html/css được render ở đây
        tối ưu SEO
        lần truy cập đầu tiên nhanh hơn
    - client side rendering
        mã html/css được render ở đây

    cách nhận biết:
        response trả về html/css là ssr
# Express & start web server
    tạo procject:
        npm init
        npm i express

    nodemon & debug:
    add git repository
        git init
        git add . 
        git commit -m
        git push 
    morgan:
    template engine
        handlebars
    static files &scss
        scss
            watch: input output
        static file
    use bootstrap
    basic routing
        set routing random
        syntax
            req, response
        GET method
            xảy ra khi truy cập vào web
            request đến server ==> phân biệt dựa vào route
            - truyền dưới dạng query parameter trên thanh url
            - khi lấy ra dữ liệu bên phía server thì .query.(tên cái cần lấy)
        form default behavior
            khi submit form tra ve theo method: GET, POST,...
            action mặc định là tại form
                có thể setups action trả kết quả request về trang khác khi submit form
        POST method
            - truyền dưới dạng form data(ẩn dưới thanh url)
            - khi cần lấy ra bên phía server thì .body.(cái gì đó)
            - .body trong server chưa được lưu g/trị của form data gửi về:
                vì thành phần ở giữa browser và controller là 1 middleware
                g/trị body nhận được bên phía server là undefined
    MVC
        ưu điểm: bóc tách các thành phần riêng biệt
        Model       : phần tương tác với data (mysql mongodb)
        View        : chửa file view(html,css)
        Controllers : phần trung gian giữa model và view
                        browser -> web server -> router -> dispatch(controller) ->
                        model -> controller -> view -> controller -> web server(response, http protocol) -> browser
    Routes & Controllers
        web server: có khi chạy npm start( node file js)
                    express cấu hình sẵn web server rồi nên chỉ cần gọi app...
                    sau khi chạy thì các require/import đã được nạp vào RAM
        Routes  : sau khi có request từ client gửi về -> trỏ vào file js -> tìm kiếm route hợp lệ
        dispatcher:   action(hợp lệ) -> dispatcher -> function handle
        browser (send req)-> web server -> router -> dispatcher -> Controllers -> ................
        quy ước tạo file:
    prettier
        làm đẹp code
        prettier --single-quote --trailing-comma all --tab-width 4 --write src/**/*.{js,json,scss}
    lint-staged
        chạy những file được add vào git 
    husky
    
    Model
        mongoose

    App
        - home
        - detail
    CRUD
        soft delete




# phân tích tiệp cận
    - phân tích tiệp cận

        + ước lượng được thời gian chạy
        + kết luận tốt nhất
            + trường hợp tốt nhất
            + trường hợp trung bình
            + trường hợp xấu nhất

        + là tiệm cận dữ liệu đầu vào 
            + nếu giải thuật không có Input -> giải thuật sẽ chạy trong một lượng thời gian cụ thể và là hằng số

        + exp:
            - thời gian chạy của một phép tính nào đó
                + là một hàm f(n)
                + với một phép tính khác là hàm g(n<sup>2</sup>)
                ==> thời gian chạy của phép tính đầu tiên sẽ tăng tuyến tính với sự tăng lên của n
                ==> thời gian chạy của phép tính thứ hai sẽ tăng theo hàm mũ khi n tăng lên
                ==> khi n là khá nhỏ thì thời gian chạy của hai phép tính là gần như nhau
        
        + Big Oh Notation
            + Ο(n) là một cách để biểu diễn tiệm cận trên của thời gian chạy của một thuật toán
            + ước lượng độ phức tạp thời gian trường hợp xấu nhất
            + O(f(n)) = {g(n)}
                if: c > 0
                    n(0): g(n) <= c*f(n) // [n > n(0)]
        
        + Omega Notation
            + Ω(n) là một cách để biểu diễn tiệm cận dưới của thời gian chạy của một giải thuật
            + ước lượng độ phức tạp thời gian trường hợp tốt nhất
            + Ω(f(n)) ≥ { g(n) }
                if: c > 0
                    n(0): g(n) <= c*f(n) // [n > n(0)]

        + Theta Notation
            + biểu diễn cả tiệm cận trên và tiệm cận dưới của thời gian chạy của một giải thuật
            + θ(f(n)) = { g(n) }
                if: g(n) = O(f(n))
                    g(n) = Ω(f(n)) // [n > n(0)]


# giai thuat tham lam (Greedy)
    + là giải thuật tối ưu hóa tổ hợp

    + tìm kiếm, lựa chọn giải pháp tối ưu địa phương ở mỗi bước
    => hi vọng tìm được giải pháp tối ưu toàn cục

    + lựa chọn giải pháp nào được cho là tốt nhất ở thời điểm hiện tại
    => giải bài toán con nảy sinh từ việc thực hiện lựa chọn đó

    + Lựa chọn có thể phụ thuộc vào lựa chọn trước đó

    + quyết định sớm và thay đổi hướng đi của giải thuật
    + không bao giờ xét lại các quyết định cũ
    ==> không tối ưu để tìm giải pháp toàn cục

    + exp:
        + 1, 2, 5, và 10 xu 
        + chọn ra 18 xu
            - áp dụng tham lam:     + chọn 10 xu (còn 8 xu)
                                    + chọn 5 xu (còn 3 xu)
                                    + chọn 2 xu (còn 1 xu)
                                    + chọn 1 xu
        ==> chọn 4 lần

        + 1, 7, 10 xu
        + chon 15 xu
            - áp dụng tham lam:     + 10
                                    + 1
                                    + 1
                                    + 1
                                    + 1
                                    + 1
        => chọn 6 lần (trong khi có thể chọn 3 lần: 7 + 7 + 1)

        ==> giải thuật tham lam:    + tìm kiếm giải pháp tôi ưu ở mỗi bước
                                    + thất bại trong việc tìm ra giải pháp tối ưu toàn cục


# chia để trị (divide & conquer)

    + chia bài toán đó thành các bài toán con nhỏ hơn
    + chia cho đến khi các bài toán nhỏ này không thể chia thêm nữa
    + giải quyết các bài toán nhỏ nhất
    + kết hợp giải pháp của tất cả các bài toán nhỏ để tìm ra giải pháp của bài toán ban đầu

    + tiến trình
        + divide/beak
            + chia bài toán ban đầu thành các bài toán con
            + sử dụng phương pháp đệ qui
            + các bài toán con được gọi là "atomic – nguyên tử"
        
        + Conquer/Solve
            + giải các bài toán con
        
        + Merge/Combine
            + kết hợp chúng một cách đệ qui để tìm ra giải pháp cho bài toán ban đầu
    
    + Hạn chế
        + Làm thế nào để chia tách bài toán một cách hợp lý thành các bài toán con
        + Việc kết hợp lời giải các bài toán con được thực hiện như thế nào

    Giải thuật sắp xếp trộn (Merge Sort)
    Giải thuật sắp xếp nhanh (Quick Sort)
    Giải thuật tìm kiếm nhị phân (Binary Search)
    Nhân ma trận của Strassen

# Quy hoạch động ( Dynamic Programming )
    + chia nhỏ bài toán thành các bài toán con nhỏ hơn
    + kết quả của các bài toán con này được lưu lại => được sử dụng cho các bài toán con tương tự hoặc các bài toán con gối nhau (Overlapping Sub-problems)

    + dùng khi
        + được chia thành các bài toán con tương tự nhau -> tái sử dụng kq
        + tối ưu hóa
        
    + 
        Dãy Fibonacci
        Bài toán tháp Hà Nội (Tower of Hanoi)
        Bài toán ba lô

# data array
    + 
    + ưu điểm:
        Truy câp phàn tử vơi thời gian hằng số O(1)
        Sử dụng bộ nhớ hiệu quả
        Tính cục bộ về bộ nhớ

# Linked List
    + một dãy các cấu trúc dữ liệu được kết nối với nhau thông qua các liên kết
    + là một cấu trúc dữ liệu bao gồm một nhóm các nút tạo thành một chuỗi
    + Mỗi nút gồm dữ liệu ở nút đó và tham chiếu đến nút kế tiếp trong chuỗi
        + Link: có thể lưu giữ một dữ liệu được gọi là một phần tử
        + Next: Mỗi liên kết chứa một link tới next link được gọi là Next
        + First: một Danh sách liên kết bao gồm các link kết nối tới first link được gọi là First

    + Biểu diễn Ds Liên kết
    
    + Danh sách liên kết chứa một phần tử link thì được gọi là First
    + Mỗi link mang một trường dữ liệu, một trường link được gọi là Next
    + Mỗi link được liên kết với link kế tiếp bởi sử dụng link kế tiếp của nó.
    + Link cuối cùng mang một link là null để đánh dấu điểm cuối của danh sách

    + các loại dslk:
        + Danh sách liên kết đơn: hỉ duyệt các phần tử theo chiều về trước
        + Danh sách liên kết đôi: các phần tử có thể được duyệt theo chiều về trước hoặc về sau
        + Danh sách liên kết vòng:  + phần tử cuối cùng chứa link của phần tử đầu tiên như là next
                                    + phần tử đầu tiên có link tới phần tử cuối cùng như là prev
    
    + Các hoạt động của dslk:
        + Hoạt động chèn
            + khi đặt một nút vào vị trí cuối của danh sách, thìnút thứ hai tính từ nút cuối cùng của danh sách sẽ trỏ tới nút mới và nút mới sẽ trỏ tới NULL
        + Hoạt động xóa (phần tử đầu)
        + Hiển thị
        + Hoạt động tìm kiếm
        + Hoạt động xóa (bởi sử dụng khóa)

    + lk đôi:
        + link : mỗi link của một Danh sách liên kết có thể lưu giữ một dữ liệu
        + next : mỗi link của một Danh sách liên kết có thể chứa một link tới next link
        + Prev : mỗi link của một Danh sách liên kết có thể chứa một link tới previous link
        + first & last : một Danh sách liên kết chứa link kết nối tới first link được gọi là First và tới last link được gọi là Last

        + các hoạt động:
            + chèn:
                + đầu
                + cuối
                + sau
            + xóa
                + đầu
                + cuối
                + key
            + hiển thị
                + về phía trước
                + về phía sau




=============================================================
==========================REDUX================================
=============================================================
- thư viện js quản lý state, state có thể dự đoán được

- dùng kiến trúc uni - directional data flow
    + View
    + Actions 
    + Store : 
        + Dispatcher
            + Middlewares: call API, log
        + Reducer:
            + nhận vào state và action
        + State

- khi nào dùng?
    + data được dùng ở nhiều nơi
    + chức năng undo/redo
        + cùng state, cùng action cho ra stae mới giống nhau
    + cần cache data để tái sử dụng cho những lần sau

- redux có phải chỉ dùng cho reactjs
    + ko, dùng cho js apps
        +reactjs, angular, vuejs, pure js app,...



# NOTE
+ Function Expression vs Function Declaration
            
    - Function declaration (khai báo hàm) sử dụng từ khóa function, theo sau là tên của hàm
        - các khai báo hàm được trình thông dịch JavaScript chuyển lên đầu phạm vi của chúng và do đó bạn có thể xác định một khai báo hàm và gọi nó ở bất kỳ đâu
    - Function Expression (biểu thức hàm)  bắt đầu bằng var, let hoặc const, theo sau là tên của hàm và toán tử gán =
        - chỉ có thể gọi một biểu thức hàm theo trình tự tuyến tính: bạn phải xác định nó trước khi gọi nó
    - Function declaration được thực hiện theo cơ chế hoisting, trong khi Function Expression thì không

# 1. phép so sánh trong JavaScript
    - so sánh nghiêm ngặt
        - sử dụng ba dấu bằng ===
        - Cả kiểu và giá trị phải giống nhau
        - không cho phép ép kiểu dữ liệu  (coercion)
            - ép kiểu tường minh
            - ép kiểu ngầm định
    - So sánh trừu tượng
        - sử dụng Dấu bằng kép
        - là so sánh giá trị bình đẳng và được phép ép kiểu dữ liệu
        - được so sánh sau khi chuyển đổi chúng thành cùng một kiểu dữ liệu
![](1-ep%20kieu%20tuong%20minh.png)
![](2-ep%20kieu%20ngam%20dinh.png)


![](3-callback.png)




# 4. && là?
    - tìm giá trị falsy đầu tiên và trả về
    - trả về giá trị cuối nếu không tìm thấy

# 5. || là?
    - tìm giá tị truthy đầu tiên và trả về

# 6. Falsy và truthy
    - Falsy
        0, 0n, undefined, null, NaN, false, ""
    - Truthy
        còn lại

# 7. Undefined và null?
    - Null
        - một giá trị rỗng hoặc không tồn tại
        - là 1 object
    - Undefined
        - một biến đã được khai báo
        - giá trị chưa xác định

# 8. IIFEs?
   - Một Immediately Invoked Function Express  được thực thi ngay sau khi nó được tạo


# 10. Ba giai đoạn của sự lan truyền sự kiện
    -  capturing trước sau đó bubbling
        - Trong giai đoạn capturing các sự kiện truyền từ Window qua  DOM tree cho đến khi nó đến nút đích
    - Bubbling ngược lại với giai đoạn capturing
        - các sự kiện nổi bong bóng (buble up) lên cây DOM


# 12.Number.MIN_VALUE > 0 ??
    - True
    - Number.MIN_VALUE là 5e-234
    - giá trị nhỏ nhất là Number.NEGATIVE_INFINITY

# 13. Math.max() nhỏ hơn Math.min()?
    - Math.min () trả về infinity và Math.max () trả về -infinity



# 15. Sự khác nhau giữa var, let và const
    - let và var có thể được gán lại (re-assigned) trong khi const thì không
    - const cho phép biến thay đổi (variable mutation), có nghĩa là nếu nó đại diện cho một mảng hoặc một đối tượng, nó có thể thay đổi. Bạn chỉ không thể chỉ định lại chính biến đó
    - let có những lợi thế đáng kể so với var, khiến nó trở thành lựa chọn tốt hơn trong hầu hết, nếu không phải là tất cả các trường hợp mà một biến cần thay đổi

    - các biến được khai báo bằng var luôn được đưa lên đầu phạm vi tương ứng của chúng
    - các biến được khai báo bằng const và let được cũng được đưa lên, nhưng nếu bạn cố gắng truy cập chúng trước khi chúng đã khai báo, bạn sẽ gặp lỗi ‘vùng chết tạm thời’ (temporal dead zone).  Đây là hành vi hữu ích, vì var có thể dễ bị lỗi hơn, chẳng hạn như tình cờ bị gán lại

    - var là phạm vi chức năng (function-scoped), let và const là phạm vi khối (block-scoped)

# 16. xác định một biến mà không có từ khóa?
    - nếu x chưa được xác định, thì x = 1 là viết tắt của window.x = 1
    sử dụng strict mode (use strict):
        - gặp lỗi khi khai bao biến ko có từ khóa:
            - Uncaught SyntaxError: Unexpected indentifier

# 17. event delegation?
    - sử dụng để phản hồi các sự kiện (event) của người dùng thông qua một node cha thay vì mỗi node con



# 19. Prototype chain?
    - trong js là kế thừa nguyên mẫu
        - truy cập thuộc tính của 1 đối tượng
            - tìm trong đối tượng
            - tìm kiếm trong nguyên mẫu của đối tượng
            - ...cho đến khi tìm thấy
    - mọi thứ đều được kế thừa từ Object

# 20. DOM?
    - là 1 API liên kết các p/tử tài liệu HTML và XML -(node)- thành 1 cấu trúc cây
    - chứa thông tin về các mối quan hệ cha-con giữa các nút
        - node là các đối tượng co thể thao tác:
            - styles
            - contentt
            - placement changes

# 26. map và forEach()
    forEach thay đổi các mục gốc trong mảng
    map trả về một mảng đã biến đổi trong khi vẫn giữ nguyên bản gốc


palindrome?
    là một từ hoặc một cụm từ mà khi ta đọc xuôi hoặc đọc ngược thì nó cũng như nhau

https://viblo.asia/p/co-che-bat-dong-bo-trong-javascript-jvElaO1zKkw

for-in
    lặp qua tất cả các thuộc tính của đối tượng theo cách thức từng bước

xử lý ngoại lệ
    dùng try...catch


Currying?
    có nghĩa là biến đổi một hàm có n đối số, thành n hàm của một hoặc ít đối số
    Currying không thay đổi hành vi của một hàm. Nó chỉ thay đổi cách nó được gọi

Phương thức PreventDefault ()
    dùng để hủy bỏ một phương thức
    ngăn không cho sự kiện thực hiện hành vi mặc định

    

# 1. khác nhau giữa undefined và not defined
    https://stackoverflow.com/questions/20822022/whats-the-difference-between-variable-definition-and-declaration-in-javascript



# html
    Element
    Attributes
    blocks & inline
    class & Id
    Layout
    Semantic elements
    file paths
# css
    inline, block, inline-block
    flexbox & grid
    box model
    position
    phan biet cac don vi
    css selection
    pseudo class
    responsive
        



















