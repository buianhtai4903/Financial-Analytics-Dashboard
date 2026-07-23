# Financial-Analytics-Dashboard
Dashboard Power BI mô phỏng báo cáo lãi lỗ (P&L) doanh nghiệp. Report gồm 5 trang, 88 visual, và 54 DAX measures, đi theo mạch phân tích tài chính chuẩn: Revenue → COGS → Opex → Profitability → KPI theo dõi mục tiêu.
mục tiêu.

⚠️ Dữ liệu trong dashboard là dữ liệu P&L giả định, chỉ phục vụ mục đích luyện tập.

Số trang	5

Tổng số visual	88

Số DAX measures	54 (gom trong 2 bảng đo lường _M và _M MoM)

Cấu trúc report
#	Trang	Visual	Nội dung chính
1	P&L Overview	19	KPI card chính + MoM, waterfall P&L, breakeven, pivot chi tiết.

2	Revenue	16	Doanh thu theo nguồn (Sales/Consulting/Other), theo Business Line, theo thời gian.

3	COGS	16	Giá vốn theo cấu phần (Materials/Labor/Packaging/Shipping), biên lợi nhuận gộp.

4	Opex	15	Chi phí vận hành theo hạng mục (Payroll/Marketing/R&D/Rent/Equipment).

5	KPI	22	KPI động — chọn 1 chỉ số qua slicer để so với mục tiêu/benchmark

# Bảng	Loại	Vai trò

_M	Bảng đo lường	Chứa ~46 measure nghiệp vụ chính (Revenue, COGS, Opex, EBIT, Net Profit...)

_M MoM	Bảng đo lường phụ	6 measure biến động tháng-qua-tháng

Calendar	Date dimension	Month, Month in text, Quarter

LocalDateTable_...	Bảng ngày tự sinh	Year (dùng trong pivot table)

Business Line	Dimension	Phân khúc kinh doanh

Subgroup	Dimension	Phân nhóm chi tiết (loại Opex, loại COGS...)

Headlines	Label table	Nhãn cột cho waterfall chart P&L

KPI	Danh mục KPI	Danh sách KPI có thể chọn (mặc định EBIT)

KPI_Target_Benchmark	Bảng mục tiêu	Giá trị Target/Benchmark theo từng KPI
