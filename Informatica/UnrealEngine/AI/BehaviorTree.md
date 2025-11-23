>Il <span style="color: orange"> Behavior Tree </span>si occupa di gestire il processo decisionale e il flusso di esecuzione dell'==intelligenza artificiale== di unreal.
Ci sono 3 concetti principali:  <span style="color: #5D3FD3"> Sequence </span> che esegue le azioni sotto di essa da destra verso sinistra, una dopo l'altra.
<span style="color: #5D3FD3"> Selector </span>che permette di scegliere un task al posto di un altro
<span style="color: orange"> (es, Usa Fucile (Fallisce) -> Usa Coltello (Successo))</span>.
>Ci sono anche i <span style="color: #EE4B2B"> BTTask </span> che sono delle classi che eseguono delle azioni (es. Insegui Player), <span style="color: #EE4B2B"> BTService</span> per degli aggiornamenti costanti, e i <span style="color: #EE4B2B"> BTDecorator </span>per aggiungere le condizioni.
>- Il BehaviorTree va <span style="color: #EE4B2B"> sempre </span> usato insieme ad una [[Blackboard]].
