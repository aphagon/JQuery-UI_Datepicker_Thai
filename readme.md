#JQuery UI - Datepicker �.�. ��
Credit ������� 1.8.10 �¤س KRISS http://www.anassirk.com/articles/1
����Ѻ���ջѭ�� Datepicker ����ͧ�Ѻ �.�.�� 
�Ը�����ҹ�����纷��������¤�Ѻ

## Howto manual Patch Ẻ�ҡ�
1. ����  isBuddhist: false ��ͷ��� yearSuffix: "" (��� Default)
2. ���ҧfunc���� _yearOffset: function (a) { if (this._get(a, "isBuddhist")) return 543; return 0 } ��ͷ���func  _daylightSavingAdjust
3. ���¡ _yearOffset �����ѧ�ҡ������¡�� _getFormatConfig �ء�ѹ (������ parameter ��� 4) ���ͨ��������� func formatDate �Ѻ parseDate �ء��ǡ���
4. ���¡ _yearOffset 仺ǡ��� c �Ѻ b ����������� <span class="ui-datepicker-year">
5. � func formatDate ���� parameter ��Ƿ�� 4 ���� �� z �����Ҫ�ǧ���Ѵ��� �� ���� c -= z;
6. � func parseDate ���� parameter ��Ƿ�� 4 ���� �� z ������ case "y" �������͹䢵���á��� 㹪�ǧ True �������  +z ��ͷ��� b.getFullYear() 