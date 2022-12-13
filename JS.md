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

# Function
    + có phạm vi là block

    + thực thi khi bị gọi (invokes it)

    + khi đạt được return => stop thực thi(executing)

    + khi gọi hàm mà ko có g/trị trong () => return fn object thay vì fn result

    + Fn Declarations(khai báo hàm)
        + không thực thi ngay -> "saved for later use" -> chạy khi gọi (invoked)
    
    + fn Expression(biểu thức hàm)
        + const ... = fn(...) {...}
        + là 1 anonymous fn ( fn no name )
        + chạy khi dùng tên biến
    
    + fn constructor
        + new Function (ko nên dùng)

    + fn hoisting
        + chỉ áp dụng fn declaration
    
    + self-invoking
        + fn exp có thể tự gọi lại chính mình
            + thực thi auto khi theo sau là ()
        + fn declaration ko thể tự gọi
            + (fn declaration)() // trick invoke 
    + fn là 1 object
        + nên có thể có prop và mothod
    
    + anonymous fn
        + một hàm không có tên
        + tất cả đều được tạo trong thời gian chạy ứng dụng
    + arrow fn
        + ko tồn tại this
        + ko được hoisted
        + nên dùng const thay cho var (fn expression có g/trị ko đổi)

    + fn parameters
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
        
        + call
            + tái sử dụng method
                + dùng method trên các object khác nhau
                + 1 object có thể dùng method của object khác
            + chấp nhận đối số(argu)
                + riêng biệt // ("...","....")

            + person.fullName.call(person1, "TN", "VN")
                // Huy Nguyen, TN, VN

        + apply
            + tái sử dụng method giống call
            + argument là 1 array
            + argu đầu ko phải object
                + strict mode
                + non strict
            
        + bind
            + object có thể mượn method của object khác
            + tránh mất this khi dùng callback
        
        + closures
            + các biến được tạo mà ko có từ khóa khai báo -> alway biến global (kể cả khi tạo bên trong fn)
            + var lifetime
                + global var tồn tại cho đến khi page bị loại bỏ (đến trang khác or đóng window)
                + local var tồn tại từ khi được invoke -> finished
        

Callback function
    - một hàm được thực thi sau khi một hàm khác đã thực thi xong
    - một hàm được truyền cho một hàm khác như một đối số và được thực thi sau khi một số tác vụ đã hoàn thành
Higher Order Function?
    - Bất kỳ hàm nào nhận một hàm khác làm đối số được gọi là hàm bậc cao hơn
    - Phương thức map giúp truyền một hàm để chuyển đổi từng mục trong một mảng
    - Filter nhận một tập hợp dữ liệu và bạn có thể chuyển một hàm có điều kiện trả về một tập hợp con của tập hợp
    - Reduce: nhận 2 đối số(accumulator và item)

    promise,callback
        callback
            cho 1 hàm là tham sô của hàm khác, tham số(fn) được lưu lại và sẻ thực thi khi co kết quả(dữ liệu tả về or lỗi khi thao tác)
            callback hell là callback lồng trong callback
        promises
            
            

    async,await
        async: thông báo fn sẽ xử lý bất đồng bộ
        await: báo chúng ta muốn đợi kq của thao tác bất đồng bộ trong 1 fn có đánh dấu async.

# Object
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
    + tạo Object?
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
    + method là các actions thực hiện được trên object
        + display method
            + by name
            + in loop
            + .value
            + .stringify
    + getter & setter
    + constructor
        + add prop to cons
        + add method to cons
    + có thể thay đổi các đối tượng -> xử lý theo tham chiếu, ko phải g/trị

    + prototype
        + all object kế thừa các prop và method từ ng/mẫu(prototype)
        + thêm prop và method vào object
            + khi đã tồn tại object
            + thêm vào constructor
                + dùng prototype
                    + Person.prototype.contry = "VN"
                    + Person.prototype.name = fn() {
                        return this.Fname + this.Lname;
                    }
    + set
        + tập hợp các g/trị duy nhất
        + new Set():
            + pass array    // const letters = new Set(["a","b","c"]);
                            // letters.add("a");
    
        + value():  return [object Set Iterator]

        + ko có keys

    sao chép các d/tượng trong js?
        shallow clone: giữ lại tham chiếu
        deep clone: tạo tham chiếu mới

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
