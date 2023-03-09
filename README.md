### [과제] 숙련주차 과제 답

1번 Form.jsx파일 12, 28, 34번째 줄, 초기값 id를 nextId();값의 id로, onSubmitHandler안에 setTodo의 id를 nextId();값의 id로 바꿔주고 dispatch를 추가하여 todo를 보내주었다.
    setTodo({
      id: id,
      title: "",
      body: "",
      isDone: false,
    });

    dispatch(addTodo(todo))

2번 todos.js파일 57번째 줄, ADD_TODO안의 retrun todos값을 [...state.todos, action.payload]로 변경하여 해결

3번 todos.js파일 61번째 줄, switch문에 DELETE_TODO케이스를 추가하여 삭제 기능을 구현
case DELETE_TODO: 
      return {
        ...state,
        todos: state.todos.filter((todo) => 
          todo.id !== action.payload
        )
      }

4번 Detail.jsx파일 13번째 줄,
const findTodo = todo.find((item) => {
    return item.id === id;
  })
위와 같은 코드를 추가하여 Params에서 받아온 id값과 일치한 객체를 가져올 수 있도록 함

5번 List.jsx파일 61번째 줄, 잘못 설정되어 있던 경로 값을 수정

6번 list.jsx파일 77번째 줄, Done 코드의 취소버튼 onClick함수에 ()=>와 인자값 (todo.id)를 추가하여 해결