# useRef랑 useState차이
```
import { useRef, useState } from "react";

export default function Player() {
  const playerName = useRef();

  const [enteredPlayerName, setEnteredPlayerName] = useState("Welcome unknown entity"); 

  const handleClick = () =>{
    setEnteredPlayerName(playerName.current.value);
    playerName.current.value="";
  }
  return (
    <section id="player">
      <h2>{enteredPlayerName}</h2>
      <p>
        <input ref={playerName} type="text" />
        <button onClick={handleClick}>Set Name</button>
      </p>
    </section>
  );
}
```
