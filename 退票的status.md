|                                             |
| ------------------------------------------- |
| case -1: temp = '审核中'; break;               |
| case 0: temp = '审核中'; break;                |
| case 1: temp = '待确认'; break;                |
| case 2: temp = '已导预订'; break;               |
| case 3: temp = '退票完成'; break;               |
| case 8: temp = '退款处理中'; break;              |
| case 4:                                     |
| {                                           |
| temp = '等待回复';                              |
| var index = obj.ReplyReason.indexOf("，");   |
| if (index > -1) {                           |
| temp = obj.ReplyReason.substring(0, index); |
| }                                           |
|                                             |
| } break;                                    |
| case 111: temp = '客户已确认'; break;            |
| case 999: temp = '错误退回'; break;             |
| case 6: temp = '等待航司退款'; break;             |
| case -9: temp = '已删除'; break;               |
