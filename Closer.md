var inner; //자리 표시자
var F = function(){
  var b = "local variable";
  var N = function(){
    return b;
  };
  inner = N;
};
// N은 F 내부에서 정의, 전역 inner 함수에 할당.
// N은 F 안에 있으므로 F함수 범위에 접근 가능
// inner과 N은 같다고 하였으니 inner도 F에 접근 가능
F(); //undefined
inner(); // "local variable"
